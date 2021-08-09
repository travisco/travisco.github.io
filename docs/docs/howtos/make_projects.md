---
layout: default
title: Make A Project
nav_order: 2
description: "Provides details about how you can create a new project to be added to our documentation. "
parent: How To's
has_toc: false
---

# Making a project in GitHub
{: .fs-9 }

## Table of Contents 
{: .no_toc .text-delta }

1. TOC
{:toc}

Projects are for large scale milestones, activities and task, that need documentation written as we move forward. Projects are considered rough drafts and has a great chance of changing struture once the project is marked "Complete", or is considered pasted a designated milestone. Find various templates needed under the "Projects" section of Templates, in this Github for basic information needed for the different project types. 
{: .fs-6 .fw-300 }
---

## Getting started

### Project Overview

At the top of every project it should give a breif overview, provide goals, JIRA's, SNOW tickets or any other relevant information needed. A project should be updated on a regular basis. Anyone looking at a project should be able to understand any task needed to get to the current point in the project. Example: When setting up the squid proxy, we should have the installation details provided as to allow anyone to continue where you left off for whatever reason. Every template will start with a basic index page, folder or page structure, initial descriptions of what information to fill in, example images and so forth. 

### How to create/clone a template

1. Logged into your local machine and in the github folder "Cleversafe\docs\templates\", you will just copy the folder into the "Projects" folder, and update the information in the files with your own. 
```cp Cleversafe\docs\templates\[TEMPLATEFOLDERNAME] Cleversafe\docs\projects\[PROJECTNAME-JIRA\SNOW] 
```

2. The navigation menu is pulled from the headers of the files, to add yours edit the information as follows.
```---
layout: default
title: [PROJECTNAME]
nav_order: [NAVORDER#]
description: "[BRIEFDESCRIPTION]"
parent: Projects
---
```

Read more on navigiation structure here, , you can have sections not display table of contents(ToC), as by default all "childern" in the navigiation structure have ToC on each page. You can disable this by adding to the header, 

```has_toc: false

Example:
---
layout: default
title: Squid Proxy
nav_order: 1
description: "Creating a reverse proxy to add LDAP authentication "
parent: Projects
---
```

You can also hide headers from the ToC by adding this line directly after the header.
```{: .no_toc }
```



<small></small>

### Local installation: Use the gem-based theme

1. Install the Ruby Gem
```bash
$ gem install just-the-docs
```
```yaml
# .. or add it to your your Jekyll site’s Gemfile
gem "just-the-docs"
```
2. Add Just the Docs to your Jekyll site’s `_config.yml`
```yaml
theme: "just-the-docs"
```
3. _Optional:_ Initialize search data (creates `search-data.json`)
```bash
$ bundle exec just-the-docs rake search:init
```
3. Run you local Jekyll server
```bash
$ jekyll serve
```
```bash
# .. or if you're using a Gemfile (bundler)
$ bundle exec jekyll serve
```
4. Point your web browser to [http://localhost:4000](http://localhost:4000)

If you're hosting your site on GitHub Pages, [set up GitHub Pages and Jekyll locally](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll) so that you can more easily work in your development environment.

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