---
layout: default
title: Make A Project
nav_order: 2
description: "Provides details about how you can create a new project to be added to our documentation. "
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

1. Logged into your local machine and in the github folder "Cleversafe\docs\templates\", you will just copy the folder into the "Projects" folder, and update the information in the files with your own. 

```bash
cp Cleversafe\docs\templates\[TEMPLATEFOLDERNAME] Cleversafe\docs\projects\[PROJECTNAME-JIRA\SNOW] 
```

1. The navigation menu is pulled from the headers of the files, to add yours edit the information as follows.

```
---
layout: default
title: [PROJECTNAME-JIRA/SNOW]
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
title: Squid Proxy - JIRA12345
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
1. For projects with children pages you need to add the "has_children: true", "parent: <small>[TITLEOFPARENTPAGE]</small>" and the "grand_parent: <small>[TITLEOFGRANDPARENT]</small>" to the header. 

```
Example:
---
layout: default
title: Squid - Installation
description: "How to install Squid Proxy through various means."
parent: Squid Proxy - JIRA12345
grand_parent: Projects
has_children: true
---
```
1. Once you have the initial structure done you can go through and replace all of the needed information. Any section wrapped with between two brakets '[ ]', and all CAPITAL letters in the name refers to information you need to replace with your own.

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
parent: Squid Proxy - JIRA12345
grand_parent: Projects
has_children: true
```
</div>

### Configure Just the Docs

- [See configuration options](https://travisco.github.io)

---

## About the project

Just the Docs is &copy; 2017-{{ "now" | date: "%Y" }} by [Patrick Marsceill](http://patrickmarsceill.com).

### License

Just the Docs is distributed by an [MIT license](https://github.com/pmarsceill/just-the-docs/tree/master/LICENSE.txt).

### Contributing

When contributing to this repository, please first discuss the change you wish to make via issue,
email, or any other method with the owners of this repository before making a change. Read more about becoming a contributor in [our GitHub repo](https://github.com/pmarsceill/just-the-docs#contributing).

#### Thank you to the contributors of Just the Docs!

<ul class="list-style-none">
{% for contributor in site.github.contributors %}
  <li class="d-inline-block mr-1">
     <a href="{{ contributor.html_url }}"><img src="{{ contributor.avatar_url }}" width="32" height="32" alt="{{ contributor.login }}"/></a>
  </li>
{% endfor %}
</ul>

### Code of Conduct

Just the Docs is committed to fostering a welcoming community.

[View our Code of Conduct](https://github.com/pmarsceill/just-the-docs/tree/master/CODE_OF_CONDUCT.md) on our GitHub repository.