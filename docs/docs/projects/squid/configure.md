---
layout: default
title: Configure
description: "Squid Proxy configuration to use as a proxy."
parent: Squid Proxy
grand_parent: Projects
---

# Squid - Configure squid as proxy
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

### Proxy configuration on RHEL / CentOS / Fedora


#### Configuring proxy through the CLI


Verify no proxy is currently set, if one is please consult with the system administrators to confirm you wont break any connections. 

```bash
# echo $http_proxy

```


Once you have your user added to the AD groups, if not please get with your lead or [ARTICLE LINK], head over here to request access. This is for passwords without special characters. 

```bash
# export http_proxy=http://USERNAME:PASSWORD@[IPADDRESSPROXY]:3128/

```


If your password has special characters, literal backslash characters (\) need to be doubled escape them as shown below.

```bash
# export http_proxy=http://USERNAME\#01:PASSWORD@[IPADDRESSPROXY]:3128/

```


When the username or password uses the @ symbol, add a backslash (\) before the @ – for example:

```bash
# export http_proxy=http:\\USERN\@ME:PASSWORD@[IPADDRESSPROXY]:3128

```


#### Configuring Proxy permanently (for processes without shell)


We will add a shell script file under /etc/profile. This will ensure the settings apply to all logged-in users.

```bash
sudo vi /etc/profile

```


Add your proxy settings.

```bash
# set proxy config via profie.d - should apply for all users
# 
PROXY_URL="http://USERNAME:PASSWORD@[IPADDRESSPROXY]:3128/"

export http_proxy="$PROXY_URL"
export https_proxy="$PROXY_URL"
export ftp_proxy="$PROXY_URL"
export no_proxy="127.0.0.1,localhost"

# For curl
export HTTP_PROXY="$PROXY_URL"
export HTTPS_PROXY="$PROXY_URL"
export FTP_PROXY="$PROXY_URL"
export NO_PROXY="127.0.0.1,localhost"

```


Source the file when done to start using the proxy settings, or alternatively logout and back in.

```bash
$ source /etc/profile

```


Confirm via

```bash
$ env | grep -i proxy

```


#### Set proxy for YUM|DNF package manager


The above settings will work for Applications and command-line tools but not for YUM and DNF package management tools.

```bash
$ sudo vim /etc/dnf/dnf.conf
# Add
proxy=http://USERNAME:PASSWORD@[IPADDRESSPROXY]:3128/

```


#### For CentOS 6/7:

You will set the username and password in the rhsm.conf file, but just enter the IP address and port of the proxy server here. 

```bash
$ sudo vim /etc/yum.conf
proxy=http://[IPADDRESSPROXY]:3128/

```

For RHEL users, you’ll also need to set Proxy for accessing RHSM content:

```bash
$ sudo vi /etc/rhsm/rhsm.conf
# Configure
proxy_hostname = proxy.example.com
proxy_port = 8080

```

If your proxy server requires authentication, also set

```bash
# user name for authenticating to an http proxy, if needed
proxy_username=

# password for basic http proxy auth, if needed
proxy_password =

```

