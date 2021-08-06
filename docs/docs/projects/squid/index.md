---
layout: default
title: Squid
description: "Just the Docs is a responsive Jekyll theme with built-in search that is easily customizable and hosted on GitHub Pages."
parent: Projects
---


# Squid Proxy Server
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---
## Overview

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

---

## Prerequisites

To specify a page order, you can use the `nav_order` parameter in your pages' YAML front matter.

#### Example
{: .no_toc }

```yaml
---
layout: default
title: Customization
nav_order: 4
---
```

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Magna eget est lorem ipsum. Pharetra et ultrices neque ornare aenean euismod. Duis at consectetur lorem donec massa. Ipsum faucibus vitae aliquet nec ullamcorper sit amet risus. Enim eu turpis egestas pretium aenean. Ut sem viverra aliquet eget sit amet. Consectetur a erat nam at lectus. Mattis aliquam faucibus purus in massa. Urna duis convallis convallis tellus id interdum velit. Sociis natoque penatibus et magnis dis parturient montes nascetur. Aliquam etiam erat velit scelerisque. Amet aliquam id diam maecenas ultricies. Interdum varius sit amet mattis vulputate. Netus et malesuada fames ac turpis egestas. Cursus euismod quis viverra nibh cras pulvinar mattis nunc sed. Euismod quis viverra nibh cras pulvinar mattis nunc sed. Lobortis mattis aliquam faucibus purus in massa. Tristique sollicitudin nibh sit amet.

Nunc eget lorem dolor sed viverra. Pellentesque id nibh tortor id aliquet lectus. Mauris a diam maecenas sed enim ut sem viverra aliquet. Pellentesque elit eget gravida cum sociis natoque penatibus et magnis. Natoque penatibus et magnis dis. Sapien pellentesque habitant morbi tristique senectus et. Nunc aliquet bibendum enim facilisis gravida neque convallis a. Ipsum faucibus vitae aliquet nec ullamcorper sit amet. Nunc congue nisi vitae suscipit tellus. A erat nam at lectus urna duis convallis convallis. Scelerisque eu ultrices vitae auctor eu augue ut lectus arcu. Turpis tincidunt id aliquet risus feugiat in ante. Posuere sollicitudin aliquam ultrices sagittis orci a scelerisque purus semper. Odio tempor orci dapibus ultrices in iaculis nunc sed.

Amet consectetur adipiscing elit ut aliquam purus sit amet. Bibendum arcu vitae elementum curabitur vitae nunc. Donec ac odio tempor orci. Vitae nunc sed velit dignissim sodales. Nunc pulvinar sapien et ligula ullamcorper malesuada. Egestas fringilla phasellus faucibus scelerisque eleifend. Sit amet cursus sit amet dictum sit. Placerat in egestas erat imperdiet sed euismod. Tristique sollicitudin nibh sit amet commodo nulla facilisi nullam. Semper quis lectus nulla at. Risus at ultrices mi tempus imperdiet nulla malesuada. In ornare quam viverra orci sagittis eu volutpat odio. Dignissim sodales ut eu sem integer vitae. Lectus mauris ultrices eros in. Sagittis eu volutpat odio facilisis mauris sit amet massa. Malesuada pellentesque elit eget gravida cum sociis natoque penatibus. Tortor pretium viverra suspendisse potenti nullam ac tortor vitae purus. At ultrices mi tempus imperdiet nulla malesuada.

---

## Installation

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Feugiat sed lectus vestibulum mattis ullamcorper velit sed ullamcorper. Volutpat consequat mauris nunc congue nisi vitae. Quis blandit turpis cursus in hac habitasse. Vitae proin sagittis nisl rhoncus. Diam phasellus vestibulum lorem sed risus ultricies tristique nulla aliquet. Elit scelerisque mauris pellentesque pulvinar pellentesque habitant. In nulla posuere sollicitudin aliquam ultrices sagittis orci. Ultricies mi quis hendrerit dolor magna. Tincidunt praesent semper feugiat nibh sed pulvinar proin gravida. Lectus sit amet est placerat in egestas. Massa tincidunt nunc pulvinar sapien et ligula. Eu mi bibendum neque egestas congue quisque egestas diam in. Leo integer malesuada nunc vel risus commodo viverra maecenas accumsan. Felis eget nunc lobortis mattis. Nulla aliquet enim tortor at auctor urna nunc. Pretium viverra suspendisse potenti nullam ac tortor vitae. Ultrices dui sapien eget mi proin sed libero. Dictum sit amet justo donec. Massa tempor nec feugiat nisl pretium fusce.

```
+-- ..
|-- (Jekyll files)
|
|-- docs
|   |-- ui-components
|   |   |-- index.md  (parent page)
|   |   |-- buttons.md
|   |   |-- code.md
|   |   |-- labels.md
|   |   |-- tables.md
|   |   +-- typography.md
|   |
|   |-- utilities
|   |   |-- index.md      (parent page)
|   |   |-- color.md
|   |   |-- layout.md
|   |   |-- responsive-modifiers.md
|   |   +-- typography.md
|   |
|   |-- (other md files, pages with no children)
|   +-- ..
|
|-- (Jekyll files)
+-- ..
```

On the parent pages, add this YAML front matter parameter:
-  `has_children: true` (tells us that this is a parent page)

#### Example
{: .no_toc }

```yaml
---
layout: default
title: UI Components
nav_order: 2
has_children: true
---
```

Here we're setting up the UI Components landing page that is available at `/docs/ui-components`, which has children and is ordered second in the main nav.

### Bare-metal
{: .text-gamma }

On child pages, simply set the `parent:` YAML front matter to whatever the parent's page title is and set a nav order (this number is now scoped within the section).

#### Example
{: .no_toc }

```yaml
---
layout: default
title: Buttons
parent: UI Components
nav_order: 2
---
```

The Buttons page appears as a child of UI Components and appears second in the UI Components section.

### Container

By default, all pages with children will automatically append a Table of Contents which lists the child pages after the parent page's content. To disable this auto Table of Contents, set `has_toc: false` in the parent page's YAML front matter.

#### Example
{: .no_toc }

```yaml
---
layout: default
title: UI Components
nav_order: 2
has_children: true
has_toc: false
---
```

### Files NeedeD
{: .text-gamma }

Child pages can also have children (grandchildren). This is achieved by using a similar pattern on the child and grandchild pages.

1. Add the `has_children` attribute to the child
1. Add the `parent` and `grand_parent` attribute to the grandchild

#### Example
{: .no_toc }

```yaml
---
layout: default
title: Buttons
parent: UI Components
nav_order: 2
has_children: true
---
```

```yaml
---
layout: default
title: Buttons Child Page
parent: Buttons
grand_parent: UI Components
nav_order: 1
---
```

This would create the following navigation structure:

```
+-- ..
|
|-- UI Components
|   |-- ..
|   |
|   |-- Buttons
|   |   |-- Button Child Page
|   |
|   |-- ..
|
+-- ..
```

---

## Configuration

Add things like LDAP configuration, work arounds and so forth.  [configuration option]

#### Example
{: .no_toc }

```yaml
# Aux links for the upper right navigation
aux_links:
  "Just the Docs on GitHub":
    - "//github.com/pmarsceill/just-the-docs"
```

---

## Issues / Workarounds 

To generate a Table of Contents on your docs pages, you can use the `{:toc}` method from Kramdown, immediately after an `<ol>` in Markdown. This will automatically generate an ordered list of anchor links to various sections of the page based on headings and heading levels. There may be occasions where you're using a heading and you don't want it to show up in the TOC, so to skip a particular heading use the `{: .no_toc }` CSS class.

#### Example
{: .no_toc }

```markdown
# Navigation Structure
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}
```

This example skips the page name heading (`#`) from the TOC, as well as the heading for the Table of Contents itself (`##`) because it is redundant, followed by the table of contents itself. To get an unordered list, replace  `1. TOC` above by `- TOC`.

### Collapsible Table of Contents

The Table of Contents can be made collapsible using the `<details>` and `<summary>` elements , as in the following example. The attribute `open` (expands the Table of Contents by default) and the styling with `{: .text-delta }` are optional.

```markdown
<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>
```

The result is shown at [the top of this page](#navigation-structure) (`{:toc}` can be used only once on each page).