---
layout: default
title: Typography
parent: Documentation Style & Guidelines
---

# Typography Utilities
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Font size

Use the `.fs-1` - `.fs-10` to set an explicit font-size.

| Class   | Small screen size `font-size`  | Large screen size `font-size` |
|:--------|:-------------------------------|:------------------------------|
| `.fs-1` | 9px                            | 10px                          |
| `.fs-2` | 11px                           | 12px                          |
| `.fs-3` | 12px                           | 14px                          |
| `.fs-4` | 14px                           | 16px                          |
| `.fs-5` | 16px                           | 18px                          |
| `.fs-6` | 18px                           | 24px                          |
| `.fs-7` | 24px                           | 32px                          |
| `.fs-8` | 32px                           | 38px                          |
| `.fs-9` | 38px                           | 42px                          |
| `.fs-10`| 42px                           | 48px                          |

<div class="code-example" markdown="1">
Font size 1
{: .fs-1 }
Font size 2
{: .fs-2 }
Font size 3
{: .fs-3 }
Font size 4
{: .fs-4 }
Font size 5
{: .fs-5 }
Font size 6
{: .fs-6 }
Font size 7
{: .fs-7 }
Font size 8
{: .fs-8 }
Font size 9
{: .fs-9 }
Font size 10
{: .fs-10 }
</div>
```markdown
In Markdown, use the `{: }` wrapper to apply custom classes:

Font size 1
{: .fs-1 }
Font size 2
{: .fs-2 }
Font size 3
{: .fs-3 }
Font size 4
{: .fs-4 }
Font size 5
{: .fs-5 }
Font size 6
{: .fs-6 }
Font size 7
{: .fs-7 }
Font size 8
{: .fs-8 }
Font size 9
{: .fs-9 }
Font size 10
{: .fs-10 }
```

## Font weight

Use the `.fw-300` - `.fw-700` to set an explicit font-size.

<div class="code-example" markdown="1">
Font weight 300
{: .fw-300 }
Font weight 400
{: .fw-400 }
Font weight 500
{: .fw-500 }
Font weight 700
{: .fw-700 }
</div>
```markdown
In Markdown, use the `{: }` wrapper to apply custom classes:

Font weight 300
{: .fw-300 }
Font weight 400
{: .fw-400 }
Font weight 500
{: .fw-500 }
Font weight 700
{: .fw-700 }
```

## Line height

Use the `lh-` classes to explicitly apply line height to text.

| Class         | `line-height` value  | Notes                         |
|:--------------|:---------------------|:------------------------------|
| `.lh-0`       | 0                    |                               |
| `.lh-tight`   | 1.1                  | Default for headings          |
| `.lh-default` | 1.4                  | Default for body (paragraphs) |

<div class="code-example" markdown="1">
No Line height
No Line height
{: .lh-0 }

Tight line height
Tight line height
{: .lh-tight }

Default line height
Default line height
{: .fh-default }
</div>
```markdown
In Markdown, use the `{: }` wrapper to apply custom classes:

No Line height
No Line height
{: .lh-0 }

Tight line height
Tight line height
{: .lh-tight }

Default line height
Default line height
{: .fh-default }
```

## Text justification

By default text is justified left. Use these `text-` classes to override settings:

| Class          | What it does         |
|:---------------|:---------------------|
| `.text-left`   | `text-align: left`   |
| `.text-right`  | `text-align: right`  |
| `.text-center` | `text-align: center` |


# Typography for UI Components
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Font stack

By default, Just the Docs uses a native system font stack for sans-serif fonts:

```scss
system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif
```

ABCDEFGHIJKLMNOPQRSTUVWXYZ
abcdefghijklmnopqrstuvwxyz
{: .fs-5 .ls-10 .code-example }

For monospace type, like code snippets or the `<pre>` element, Just the Docs uses a native system font stack for monospace fonts:

```scss
"SFMono-Regular", Menlo, Consolas, Monospace
```

ABCDEFGHIJKLMNOPQRSTUVWXYZ
abcdefghijklmnopqrstuvwxyz
{: .fs-5 .ls-10 .text-mono .code-example }

---

## Responsive type scale

Just the Docs uses a responsive type scale that shifts depending on the viewport size.

| Selector              | Small screen size `font-size`    | Large screen size `font-size` |
|:----------------------|:---------------------------------|:------------------------------|
| `h1`, `.text-alpha`   | 32px                             | 36px                          |
| `h2`, `.text-beta`    | 18px                             | 24px                          |
| `h3`, `.text-gamma`   | 16px                             | 18px                          |
| `h4`, `.text-delta`   | 14px                             | 16px                          |
| `h5`, `.text-epsilon` | 16px                             | 18px                          |
| `h6`, `.text-zeta`    | 18px                             | 24px                          |
| `body`                | 14px                             | 16px                          |

---

## Headings

Headings are rendered like this:

<div class="code-example">
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
</div>
```markdown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

---

## Body text

Default body text is rendered like this:

<div class="code-example" markdown="1">
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
</div>
```markdown
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
```

---

## Inline elements

<div class="code-example" markdown="1">
Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](another-page).
</div>
```markdown
Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](another-page).
```

---

## Typographic Utilities

There are a number of specific typographic CSS classes that allow you to override default styling for font size, font weight, line height, and capitalization.

