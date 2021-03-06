---
layout: default
title: Add a Project
nav_order: 2
description: "Provides details about how you can create a new project into your squads docuemtnation page, add it to the navigation menu, and tips on formatting. "
parent: How To's
has_toc: false
---

# Making a project for your team.
{: .fs-9 }

## Table of Contents 
{: .no_toc .text-delta }

1. TOC
{:toc}

Projects are large scale milestones, activities,and task. Project documentation are considered rough drafts, and have high chances of changing struture once the project is considered pasted a designated milestone. Find various templates needed under the "Projects" section of Templates, in this Github for basic information needed for the different project types. 
{: .fs-6 .fw-300 }
---

## Getting started

### Project Overview

At the top of every project it should give a breif overview, provide goals, JIRA's, SNOW tickets or any other relevant information needed. A project should be updated on a regular basis. Anyone looking at a project should be able to understand any task needed to get to the current point in the project. Example: When setting up the squid proxy, we should have the installation details provided as to allow anyone to continue where you left off for whatever reason. Every template will start with a basic index page, folder or page structure, initial descriptions of what information to fill in, example images and so forth. 

### How to create/clone a template

2. Logged into your local machine and in the github folder "Cleversafe\docs\templates\", you will just copy the folder into the "Projects" folder, and update the information in the files with your own. 

```bash
cp Cleversafe\docs\templates\[TEMPLATEFOLDERNAME] Cleversafe\docs\projects\[PROJECTNAME] 
```

2. The navigation menu is pulled from the headers of the files, to add yours edit the information as follows.

```
---
layout: default
title: [PROJECTNAME]
nav_order: [NAVORDER#]
description: "[BRIEFDESCRIPTION]"
parent: Projects
---
```

Learn more about [Navigation Structure]({{ site.baseurl }}{% link docs/howtos/documentation/navigation-structure.md %}) here. By default all "childern" in the navigiation structure have ToC displayed at the top of each page. Disable this by adding the following to the header, 

```
has_toc: false

Example:
---
layout: default
title: Squid Proxy
nav_order: 1
description: "Creating a reverse proxy to add LDAP authentication to fulfill QOS requirements."
parent: Projects
has_toc: false
---
```

You can hide headers from the ToC by adding this line directly after the header you want to hide.

```
{: .no_toc }

Example:

## How to connect LDAP
{: .no_toc }
```

If you exclude the 'nav_order' item, it will go alphabetically after the projects that have the 'nav_order' and numbers listed.

### File Structure and adding "Folders" or Children

Some templates will have children or drop down menus added to help reduce clutter, and add the workflow that fits best for the project. 
<div markdown="1">
2. For projects with children pages you need to add the "has_children: true", "parent: <small>[TITLEOFPARENT]</small>" and the "grand_parent: <small>[TITLEOFGRANDPARENT]</small>" to the header. 

```
Example:
---
layout: default
title: Squid - Installation
description: "How to install Squid Proxy through various means."
parent: Squid Proxy
grand_parent: Projects
has_children: true
---
```
2. Once you have the initial structure done you can go through and replace all of the needed information. Any section wrapped with between two brakets '[ ]', and all CAPITAL letters in the name refers to information you need to replace with your own.

```
Example: 

layout: default
title: [TITLEOFPAGE]
nav_order: [NAVORDER#]
description: "[BRIEFDESCRIPTION]"
parent: Projects

----

layout: default
title: Squid - Installation
description: "How to install Squid Proxy through various means."
parent: Squid Proxy
grand_parent: Projects
has_children: true
```
</div>