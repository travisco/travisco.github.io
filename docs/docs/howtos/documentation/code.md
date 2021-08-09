---
layout: default
title: Code - Color - Labels
parent: Document Formatting
grand_parent: How To's
---

# Code - Color - Labels
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

# Code

---

## Inline code
{: .no_toc }

Code can be rendered inline by wrapping it in single back ticks.

<div class="code-example" markdown="1">
Lorem ipsum dolor sit amet, `<inline code snippet>` adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

## Heading with `<inline code snippet>` in it.
{: .no_toc }

</div>
```markdown
Lorem ipsum dolor sit amet, `<inline code snippet>` adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

## Heading with `<inline code snippet>` in it.
```

---

## Syntax highlighted code blocks
{: .no_toc }

Use Jekyll's built-in syntax highlighting with Rouge for code blocks by using three backticks, followed by the language name:

<div class="code-example" markdown="1">
```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```
</div>
{% highlight markdown %}
```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```
{% endhighlight %}

---

## Code blocks with rendered examples
{: .no_toc }

To demonstrate front end code, sometimes it's useful to show a rendered example of that code. After including the styles from your project that you'll need to show the rendering, you can use a `<div>` with the `code-example` class, followed by the code block syntax. If you want to render your output with Markdown instead of HTML, use the `markdown="1"` attribute to tell Jekyll that the code you are rendering will be in Markdown format... This is about to get meta...

<div class="code-example" markdown="1">

<div class="code-example" markdown="1">

[Link button](http://example.com/){: .btn }

</div>
```markdown
[Link button](http://example.com/){: .btn }
```

</div>
{% highlight markdown %}
<div class="code-example" markdown="1">

[Link button](http://example.com/){: .btn }

</div>
```markdown
[Link button](http://example.com/){: .btn }
```
{% endhighlight %}


# Color Utilities

---

All the colors used in Just the Docs have been systematized into a series of variables that have been extended to both font color and background color utility classes.

## Light Greys
{: .no_toc }
| Color value    | Font color utility   | Background color utility |
|:---------------|:---------------------|:-------------------------|
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-grey-lt-000"></span> `grey-lt-000` | `.text-grey-lt-000` | `.bg-grey-lt-000` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-grey-lt-100"></span> `grey-lt-100` | `.text-grey-lt-100` | `.bg-grey-lt-100` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-grey-lt-200"></span> `grey-lt-200` | `.text-grey-lt-200` | `.bg-grey-lt-200` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-grey-lt-300"></span> `grey-lt-300` | `.text-grey-lt-300` | `.bg-grey-lt-300` |

## Dark Greys
{: .no_toc }
| Color value    | Font color utility   | Background color utility |
|:---------------|:---------------------|:-------------------------|
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-grey-dk-000"></span> `grey-dk-000` | `.text-grey-dk-000` | `.bg-grey-dk-000` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-grey-dk-100"></span> `grey-dk-100` | `.text-grey-dk-100` | `.bg-grey-dk-100` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-grey-dk-200"></span> `grey-dk-200` | `.text-grey-dk-200` | `.bg-grey-dk-200` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-grey-dk-250"></span> `grey-dk-250` | `.text-grey-dk-250` | `.bg-grey-dk-250` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-grey-dk-300"></span> `grey-dk-300` | `.text-grey-dk-300` | `.bg-grey-dk-300` |

## Purples
{: .no_toc }
| Color value    | Font color utility   | Background color utility |
|:---------------|:---------------------|:-------------------------|
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-purple-000"></span> `purple-000` | `.text-purple-000` | `.bg-purple-000` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-purple-100"></span> `purple-100` | `.text-purple-100` | `.bg-purple-100` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-purple-200"></span> `purple-200` | `.text-purple-200` | `.bg-purple-200` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-purple-300"></span> `purple-300` | `.text-purple-300` | `.bg-purple-300` |

## Blues
{: .no_toc }
| Color value    | Font color utility   | Background color utility |
|:---------------|:---------------------|:-------------------------|
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-blue-000"></span> `blue-000` | `.text-blue-000` | `.bg-blue-000` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-blue-100"></span> `blue-100` | `.text-blue-100` | `.bg-blue-100` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-blue-200"></span> `blue-200` | `.text-blue-200` | `.bg-blue-200` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-blue-300"></span> `blue-300` | `.text-blue-300` | `.bg-blue-300` |

## Greens
{: .no_toc }
| Color value    | Font color utility   | Background color utility |
|:---------------|:---------------------|:-------------------------|
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-green-000"></span> `green-000` | `.text-green-000` | `.bg-green-000` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-green-100"></span> `green-100` | `.text-green-100` | `.bg-green-100` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-green-200"></span> `green-200` | `.text-green-200` | `.bg-green-200` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-green-300"></span> `green-300` | `.text-green-300` | `.bg-green-300` |

## Yellows
{: .no_toc }
| Color value    | Font color utility   | Background color utility |
|:---------------|:---------------------|:-------------------------|
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-yellow-000"></span> `yellow-000` | `.text-yellow-000` | `.bg-yellow-000` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-yellow-100"></span> `yellow-100` | `.text-yellow-100` | `.bg-yellow-100` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-yellow-200"></span> `yellow-200` | `.text-yellow-200` | `.bg-yellow-200` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-yellow-300"></span> `yellow-300` | `.text-yellow-300` | `.bg-yellow-300` |

## Reds
{: .no_toc }
| Color value    | Font color utility   | Background color utility |
|:---------------|:---------------------|:-------------------------|
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-red-000"></span> `red-000` | `.text-red-000` | `.bg-red-000` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-red-100"></span> `red-100` | `.text-red-100` | `.bg-red-100` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-red-200"></span> `red-200` | `.text-red-200` | `.bg-red-200` |
| <span class="d-inline-block p-2 mr-1 v-align-middle bg-red-300"></span> `red-300` | `.text-red-300` | `.bg-red-300` |

# Labels

Use labels as a way to add an additional mark to a section of your docs. Labels come in a few colors. By default, labels will be blue.

<div class="code-example" markdown="1">
Default label
{: .label }

Blue label
{: .label .label-blue }

Stable
{: .label .label-green }

New release
{: .label .label-purple }

Coming soon
{: .label .label-yellow }

Deprecated
{: .label .label-red }
</div>
```markdown
Default label
{: .label }

Blue label
{: .label .label-blue }

Stable
{: .label .label-green }

New release
{: .label .label-purple }

Coming soon
{: .label .label-yellow }

Deprecated
{: .label .label-red }
```
