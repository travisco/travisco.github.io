---
layout: default
title: Installation
description: "Squid Proxy installation."
parent: Squid Proxy
grand_parent: Projects
---

# Squid - Installation
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

### Installation


#### Bare-metal
{: .text-gamma }

##### Prerequisites

* Operating System: Debian 10(Buster) with the latest at 8/1/2021
* User created for squid, best practice is to use squid.


---

##### Install Squid & Dependencies

1. Download the version of squid you want and store it in the directory. 


```bash
# cd /opt

# wget http://www.squid-cache.org/Versions/v5/squid-5.1-20210804-r1f9e52827.tar.gz

# tar -xvf squid-5.1-20210804-r1f9e52827.tar.gz
```


2. Assuming you used version 5.1, change into the new directory created from un tarring the file and also build the configuration. Here is where we enable openssl and ssl-crtd, which is not in the standard squid package when installing from 'apt-get'. 


```bash
# cd squid-5.1/

# apt-get install build-essential libssl-dev libffi-dev python3-dev cargo

# ./configure --prefix=/usr --localstatedir=/var --libexecdir=${prefix}/lib/squid --datadir=${prefix}/share/squid --sysconfdir=/etc/squid --with-default-user=proxy --with-logdir=/var/log --with-pidfile=/var/run/squid.pid --with-openssl --enable-ssl-crtd
```

3. Next we will create the self sign certification to use with openssl,


```bash
# openssl req -new -newkey rsa:4096 -days 365 -nodes -x509 -keyout bump.key -out bump.crt

# openssl x509 -in bump.crt -outform DER -out bump.der

# openssl dhparam -outform PEM -out /etc/squid/bump_dhparam.pem 4096

# chown proxy:proxy /etc/squid/bump*

# chmod 400 /etc/squid/bump*
```


4. Create and initalize the DB for storing the certificetes


```bash
# mkdir -p /var/lib/squid

# rm -rf /var/lib/squid/ssl_db

# /usr/lib/squid/security_file_certgen -c -s /var/lib/squid/ssl_db -M 20MB

# chown -R proxy:proxy /var/lib/squid
```

5. The squid service was not in the system after installation, I found this file and made a minor adjustment to the path location for squid (add '/usr/lib' to the end of the path list),


```bash
# export $PATH:/usr/lib

# cd /etc/init.d/
```

[Init.d Squid Direct File]({{ site.baseurl }}{% link assets/files/squid %}){: .btn .btn-green .mr-2 } [Init.d Squid File - Site](https://www.apt-browse.org/browse/ubuntu/xenial/main/amd64/squid/3.5.12-1ubuntu7/file/etc/init.d/squid){: .btn .btn-blue } 

6. Next we need to put the LDAP authenticator into the correct folder for squid, for this build it was located under


```bash
# /usr/lib/squid
```

[basic_ldap_auth]({{ site.baseurl }}{% link assets/files/basic_ldap_auth %}){: .btn .btn-green }

7. Create a password and store it in the squid configuration folder.

```bash
# touch /etc/squid/ldap_password

# vi /etc/squid/ldap_password

# chmod 644 /etc/squid/ldap_password
```


8. Upload this squid configuration to the server and put it in the location listed below, **Rename file to squid.conf


[Squid.conf Bare-metal]({{ site.baseurl }}{% link assets/files/squid-baremetal.conf %}){: .btn .btn-yellow .mr-2 } [Squid.conf Container]({{ site.baseurl }}{% link assets/files/squid-container.conf %}){: .btn .btn-yellow }

```bash
# /etc/squid/

# cp /tmp/squid-baremetal.conf /etc/squid/squid.conf
```


9. Upload squid into the system defaults


```bash
# update-rc.d squid defaults

# systemctl start squid
```

This configuration file contains the needed LDAP authentication for COS. You can use this article to test it out with your information. 

##### Related Links

[Kaspersky](https://support.kaspersky.com/KWTS/6.1/en-US/166244.htm) -- 
[Squid Cache](http://www.squid-cache.org/Versions/v5/) -- 
[Apt Browse](https://www.apt-browse.org/browse/ubuntu/xenial/main/amd64/squid/3.5.12-1ubuntu7/file/etc/init.d/squid) -- 
[Scubarda](https://scubarda.com/2020/03/23/configure-squid-proxy-for-ssl-tls-inspection-https-interception/) -- 

#### Container
{: .text-gamma }

##### Prerequisites

* Docker: 

We are using salrashid123/squidproxy version 3.5.27. 

[GitHub](https://github.com/salrashid123/squid_proxy){: .btn .btn-black .mr-2 } [Docker Hub](https://hub.docker.com/r/salrashid123/squidproxy/){: .btn .btn-blue } 


##### Install Squid & Container

1. Curl command to hit the squid proxy

```bash
curl -v --proxy-cacert /home/trpotter/squid/apps/sl/CA_crt.pem --cacert /home/trpotter/squid/apps/sl/CA_crt.pem -x "cos-ldaptest1:<mypassword>@:osscosbperfuatwdc0602f:3128"  https://www.yahoo.com
```

2. Command to launch the container

```bash
docker run -d -p 3128:3128 \
--volume /home/trpotter/squid/apps/squid.conf.intercept:/apps/squid.conf.intercept \
--volume /home/trpotter/squid/apps/sl/basic_ldap_auth:/apps/squid/libexec/basic_ldap_auth \
--volume /home/trpotter/squid/apps/sl/ldap_password:/apps/ldap_password \
--volume /home/trpotter/squid/apps/sl/CA_crt.pem:/apps/CA_crt.pem \
--volume /home/trpotter/squid/apps/sl/CA_key.pem:/apps/CA_key.pem \
--volume /home/trpotter/squid/apps/sl/:/apps/sl/ docker.io/salrashid123/squidproxy /apps/squid/sbin/squid -NsY -d 2/* -f /apps/squid.conf.intercept
```

