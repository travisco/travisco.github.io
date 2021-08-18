---
layout: default
title: Quarterly Review
description: "Processes for the quarterly review."
parent: Administrative
---

# Quarterly Review
{: .fs-9 }

| Runbook Details      |                      |                      |                      |
|:---------------------|:---------------------|:---------------------|:---------------------|
| **Category**         | Operational          | **Audience**         | COS Delivery         |
| **Reviewers**        | See Reviewers table  | **Owner**            | Load Balancing Squad |
| **Monitoring Alert** | NA                   |                      |                      |

---

## Introduction


To satisfy our compliance requirements, and to assure uniformity across our systems, we are implementing a quarterly review process of the running configuration of all NetScaler systems. 

As a first step, we are implementing a build validation report to assure all newly built nodes are vetted as ready for production. This includes backup of the running configuration to a GitHub repository to provide a centralized location for configuration storage and change control for as we refine and optimize our processes and configurations on the NetScalers.  

#### Details
Tools currently available for configuration backup and review
We have multiple methods at our disposal, both on the nodes and via scripted automation, for the retrieval and review of the running configuration and any changes that may occur to it.  

##### Netscaler UI:  
On the Configuration Tab under System > Diagnostics are several tools for working with both saved and running configurations, including a tool to view revision history.  The NetScalers automatically save the last 5 running configurations.  These can be compared

to the current running configuration and commands can be generated from this report to roll back changes if necessary.  Additional tools are available to compare saved vs running configurations.  

![](https://github.com/travisco/travisco.github.io/blob/main/docs/assets/img/quarterlyreview01.png)

### Backup of COS running configuration via scripting


Using the following script, the running configuration of all COS LB clusters can be saved to a centralized location.  We plan on implementing a version of this script for the purpose of a regularly scheduled backup of the running configurations of all nodes.  This will be expanded to include the Swift, Monitoring, and Offering nodes as well.  We will include this script in the utilities folder in the build repo initially, and it will eventually reside in the repository created for configuration backup and review:

```bash
nsConfigSave.rb -h
 
Usage: ssh.rb [options]
-f, --hostfile NAME File with list of hosts
-H, --desthost HOST Destination host
-p, --perhostcmd Per host command
-u, --username USER Username
-h, --help Prints this help
```

#### The process for configuration review (version 1):
```markdown
1. All revisions to the running configuration should occur via our pipeline utilizing the repository for build automation and configuration revision.  This allows for review and approval of all changes and signoff by the team.  
2. These changes are to be documented via confluence with links to JIRA tickets and pull requests, reviewed by squad members, and stored in the documentation Confluence Space.  These will be stored in a space to be created for each quarter that will be identified in a manner similar to "Storage Loadbalancing Configuration Revision History: <Quarter> <Year>"
3. At the end of each quarter, these documents will be reviewed, and verification that any changes included have been rolled into the build and monitoring automation, relevant documentation, and have the proper accounting of their implementation date within change control.  
4. Automation will be developed for configuration comparison that will be linked to monitoring and identification of outlying nodes found to have revisions that are not in step with approved configs.  
5. Monitoring is currently being developed for SSL certificate expiry.  A quarterly review will also occur to verify all certificates are backed up in a secure location to be determined. This can include a secured Ansible Vault or Thycotic.  
6. A quarterly review of IPAM to assure all node names and endpoint names are entered properly.  Potential automation for this task is available via the IPAM API
```