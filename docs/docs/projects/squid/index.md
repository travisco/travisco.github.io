---
layout: default
title: Squid Proxy
description: "Squid Proxy server POC."
parent: Projects
has_children: true
---


# Squid Proxy Server
{: .no_toc }

---
## What is squid proxy?

### Squid: Optimising Web Delivery
Squid is a caching proxy for the Web supporting HTTP, HTTPS, FTP, and more. It reduces bandwidth and improves response times by caching and reusing frequently-requested web pages. Squid has extensive access controls and makes a great server accelerator. It runs on most available operating systems, including Windows and is licensed under the GNU GPL.

#### Making the most of your Internet Connection
Squid is used by hundreds of Internet Providers world-wide to provide their users with the best possible web access. Squid optimises the data flow between client and server to improve performance and caches frequently-used content to save bandwidth. Squid can also route content requests to servers in a wide variety of ways to build cache server hierarchies which optimise network throughput.

#### Website Content Acceleration and Distribution
Thousands of web-sites around the Internet use Squid to drastically increase their content delivery. Squid can reduce your server load and improve delivery speeds to clients. Squid can also be used to deliver content from around the world - copying only the content being used, rather than inefficiently copying everything. Finally, Squid's advanced content routing configuration allows you to build content clusters to route and load balance requests via a variety of web servers.

The Squid systems are currently running at a hit-rate of approximately 75%, effectively quadrupling the capacity of the Apache servers behind them. This is particularly noticeable when a large surge of traffic arrives directed to a particular page via a web link from another site, as the caching efficiency for that page will be nearly 100%.  - Wikimedia Deployment Information.

#### Want to learn more?
The Squid project provides a number of resources to assist users design, implement and support Squid installations. Please browse the Documentation and Support sections for more information.

[Squid Proxy](http://www.squid-cache.org){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } 

---

## Squid Proxy and COS

To have better security check points for traffic moving over our networks, the forward proxy has been designed to authenicate traffic flows, at which will be targeting external services, and are traveling over the public network. 

## Overview

In our current setup we are using [squid](http://www.squid-cache.org/) solution to tie forward proxy features to AD authenication. This will allow the LB team to setup with our internal teams AD groups, at which other teams may then add a user to the group to gain access to utilize the proxy. Further security requirements will need to be met as well.

### Requirements
 * Logging
    * Failed proxy login attempts (source_ip, user, password)
    * Success proxy login (source_ip, user)
    * Delivered to QRadar
    * Notes:
      * password provided in failure but not success so that we can tell if user is doing dicitionary attacks
 * Authenication
    * Basic Auth ([RFC7235](https://datatracker.ietf.org/doc/html/rfc7235))
    * User must be AD and follow internal processes controls
    * LB Team requested AD Group will be used to tie permissions
 * Fault Tolerance
   * High Avaiability at a regional level
     * GSLB preferred method
 * Monitoring
   * Squid
     * Metric API polled and exported to graphite
       * (either)
       * collectd [sample plugin](https://gist.github.com/wrzasa/dfd7b554171159a6b2ab24b03b8e30b8)
       * prometheus [sample](https://github.com/boynux/squid-exporter)
     * grafana graphes
   * Proxy endpoint
     * PING
     * HTTPS connect
 * Documentation
   * Overview (this)
   * Runbooks
     * Audit Report
     * AD Group Map (Current & Update Process)
     * Sample Client Configuration & Testing
     * Remote Service Monitoring
     * Logging (Locations/Handling/Expiry)
     * Container Build Process
       * Include flow of container where it maybe in different stages of the build process to production repo for deployment.
 * Process for submitting external site request.
### Deployment

  * Container Based Software
    * If Kube does not already existing, VM created with single node kube would work for now
  * Deployment Locations
    * TODO: create table of VM/Kube resource locations
  * Remote Site Access Allow
    * TODO: access table 
  * Team Functional Testing
    * TODO: bulid access table and results. 

### Wish List
  * Logging
    * QRadar Alerting
  * Authenication
    * mTLS
  * Fault Tolerance
    * BGP ECMP
  * Monitoring
    * Icinga
      * Utilize proxy to reach external service

## Diagrams 

### Regional Deployment Overview

![forward_proxy_regional_overview](https://github.ibm.com/cleversafe-infra/cos-lb-docs/raw/ced839050fe62a47c6a47e2043972994a66c3c60/assets/forward-proxy/forward_proxy.png)

### Service Deployment Details

![forward_proxy_details](https://github.ibm.com/cleversafe-infra/cos-lb-docs/blob/ced839050fe62a47c6a47e2043972994a66c3c60/assets/forward-proxy/forward_proxy_details.png)