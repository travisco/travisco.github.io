---
layout: default
title: Document Formatting
nav_order: 1
description: "Provides details about how you can structure documentation, create pages and guidelines to follow for coding structure."
parent: How To's
has_toc: false
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

# Formatting Guidelines, Tips & Tricks

---

## Getting started
{: .no_toc }

### Common styling and formating in GitHub
{: .no_toc }

{: .fs-9 }

---

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](another-page).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# [](#header-1)Header 1
{: .no_toc }


This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## [](#header-2)Header 2
{: .no_toc }

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### [](#header-3)Header 3
{: .no_toc }

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### [](#header-4)Header 4 `with code not transformed`
{: .no_toc }

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### [](#header-5)Header 5
{: .no_toc }

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### [](#header-6)Header 6
{: .no_toc }

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.
{: .no_toc }

* * *

### Here is an unordered list:
{: .no_toc }

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:
{: .no_toc }

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:
{: .no_toc }

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Nesting an ol in ul in an ol
{: .no_toc }

- level 1 item (ul)
  1. level 2 item (ol)
  1. level 2 item (ol)
    - level 3 item (ul)
    - level 3 item (ul)
- level 1 item (ul)
  1. level 2 item (ol)
  1. level 2 item (ol)
    - level 3 item (ul)
    - level 3 item (ul)
  1. level 4 item (ol)
  1. level 4 item (ol)
    - level 3 item (ul)
    - level 3 item (ul)
- level 1 item (ul)

### And a task list
{: .no_toc }

- [ ] Hello, this is a TODO item
- [ ] Hello, this is another TODO item
- [x] Goodbye, this item is done

### Small image
{: .no_toc }

![](https://assets-cdn.github.com/images/icons/emoji/octocat.png)

### Large image
{: .no_toc }

![](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.
{: .no_toc }

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

#### Multiple description terms and values
{: .no_toc }

Term
: Brief description of Term

Longer Term
: Longer description of Term,
  possibly more than one line

Term
: First description of Term,
  possibly more than one line

: Second description of Term,
  possibly more than one line

Term1
Term2
: Single description of Term1 and Term2,
  possibly more than one line

Term1
Term2
: First description of Term1 and Term2,
  possibly more than one line

: Second description of Term1 and Term2,
  possibly more than one line
  
### More code
{: .no_toc }

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
{: .fs-6 .fw-300 }

## Basic button styles
{: .no_toc }

### Links that look like buttons
{: .no_toc }

<div class="code-example" markdown="1">
[Link button](http://example.com/){: .btn }

[Link button](http://example.com/){: .btn .btn-purple }
[Link button](http://example.com/){: .btn .btn-blue }
[Link button](http://example.com/){: .btn .btn-green }

[Link button](http://example.com/){: .btn .btn-outline }
</div>
```markdown
[Link button](http://example.com/){: .btn }

[Link button](http://example.com/){: .btn .btn-purple }
[Link button](http://example.com/){: .btn .btn-blue }
[Link button](http://example.com/){: .btn .btn-green }

[Link button](http://example.com/){: .btn .btn-outline }
```

### Button element
{: .no_toc }

GitHub Flavored Markdown does not support the `button` element, so you'll have to use inline HTML for this:

<div class="code-example">
<button type="button" name="button" class="btn">Button element</button>
</div>
```html
<button type="button" name="button" class="btn">Button element</button>
```

---

## Using utilities with buttons
{: .no_toc }

### Button size
{: .no_toc }

Wrap the button in a container that uses the [font-size utility classes]({{ site.baseurl }}{% link docs/howtos/documentation/typography.md %}) to scale buttons:

<div class="code-example" markdown="1">
<span class="fs-6">
[Big ass button](http://example.com/){: .btn }
</span>

<span class="fs-3">
[Tiny ass button](http://example.com/){: .btn }
</span>
</div>
```markdown
<span class="fs-8">
[Link button](http://example.com/){: .btn }
</span>

<span class="fs-3">
[Tiny ass button](http://example.com/){: .btn }
</span>
```

### Spacing between buttons
{: .no_toc }

Use the [margin utility classes]({{ site.baseurl }}{% link docs/howtos/documentation/layout.md %}#spacing) to add spacing between two buttons in the same block.

<div class="code-example" markdown="1">
[Button with space](http://example.com/){: .btn .btn-purple .mr-2 }
[Button ](http://example.com/){: .btn .btn-blue .mr-2 }

[Button with more space](http://example.com/){: .btn .btn-green .mr-4 }
[Button ](http://example.com/){: .btn .btn-blue }
</div>
```markdown
[Button with space](http://example.com/){: .btn .btn-purple .mr-2 }
[Button ](http://example.com/){: .btn .btn-blue }

[Button with more space](http://example.com/){: .btn .btn-green .mr-4 }
[Button ](http://example.com/){: .btn .btn-blue }
```

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

# Layout Utilities

---

## Spacing
{: .no_toc }
These spacers are available to use for margins and padding with responsive utility classes. Combine these prefixes with a screen size and spacing scale to use them responsively.

| Classname prefix | What it does                  |
|:-----------------|:------------------------------|
| `.m-`            | `margin`                      |
| `.mx-`           | `margin-left`, `margin-right` |
| `.my-`           | `margin top`, `margin bottom` |
| `.mt-`           | `margin-top`                  |
| `.mr-`           | `margin-right`                |
| `.mb-`           | `margin-bottom`               |
| `.ml-`           | `margin-left`                 |

| Classname prefix | What it does                    |
|:-----------------|:--------------------------------|
| `.p-`            | `padding`                       |
| `.px-`           | `padding-left`, `padding-right` |
| `.py-`           | `padding top`, `padding bottom` |
| `.pt-`           | `padding-top`                   |
| `.pr-`           | `padding-right`                 |
| `.pb-`           | `padding-bottom`                |
| `.pl-`           | `padding-left`                  |

Spacing values are based on a `1rem = 16px` spacing scale, broken down into these units:

| Spacer/suffix  | Size in rems  | Rem converted to px |
|:---------------|:--------------|:--------------------|
| `1`            | 0.25rem       | 4px                 |
| `2`            | 0.5rem        | 8px                 |
| `3`            | 0.75rem       | 12px                |
| `4`            | 1rem          | 16px                |
| `5`            | 1.5rem        | 24px                |
| `6`            | 2rem          | 32px                |
| `7`            | 2.5rem        | 40px                |
| `8`            | 3rem          | 48px                |
| `auto`         | auto          | auto                |

Use `mx-auto` to horizontally center elements.

#### Examples
{: .no_toc }

In Markdown, use the `{: }` wrapper to apply custom classes:

```markdown
This paragraph will have a margin bottom of 1rem/16px at large screens.
{: .mb-lg-4 }

This paragraph will have 2rem/32px of padding on the right and left at all screen sizes.
{: .px-6 }
```

## Horizontal Alignment
{: .no_toc }
| Classname               | What it does                     |
|:------------------------|:---------------------------------|
| `.float-left`           | `float: left`                    |
| `.float-right`          | `float: right`                   |
| `.flex-justify-start`   | `justify-content: flex-start`    |
| `.flex-justify-end`     | `justify-content: flex-end`      |
| `.flex-justify-between` | `justify-content: space-between` |
| `.flex-justify-around`  | `justify-content: space-around`  |

_Note: any of the `flex-` classes must be used on a parent element that has `d-flex` applied to it._

## Vertical Alignment
{: .no_toc }
| Classname              | What it does                    |
|:-----------------------|:--------------------------------|
| `.v-align-baseline`    | `vertical-align: baseline`      |
| `.v-align-bottom`      | `vertical-align: bottom`        |
| `.v-align-middle`      | `vertical-align: middle`        |
| `.v-align-text-bottom` | `vertical-align: text-bottom`   |
| `.v-align-text-top`    | `vertical-align: text-top`      |
| `.v-align-top`         | `vertical-align: top`           |

## Display
{: .no_toc }
Display classes aid in adapting the layout of the elements on a page:

| Class             |                         |
|:------------------|:------------------------|
| `.d-block`        | `display: block`        |
| `.d-flex`         | `display: flex`         |
| `.d-inline`       | `display: inline`       |
| `.d-inline-block` | `display: inline-block` |
| `.d-none`         | `display: none`         |

Use these classes in conjunction with the responsive modifiers.

#### Examples
{: .no_toc }

In Markdown, use the `{: }` wrapper to apply custom classes:

```markdown
This button will be hidden until medium screen sizes:

[ A button ](#url)
{: .d-none .d-md-inline-block }

These headings will be `inline-block`:

### heading 3
{: .d-inline-block }

### heading 3
{: .d-inline-block }
```

# Code snippets with line numbers
{: .no_toc }
The default settings for HTML compression are incompatible with the HTML
produced by Jekyll (4.1.1 or earlier) for line numbers from highlighted code
-- both when using Kramdown code fences and when using Liquid highlight tags.

To avoid non-conforming HTML and unsatisfactory layout, HTML compression
can be turned off by using the following configuration option:

{% highlight yaml %}
compress_html:
  ignore:
    envs: all
{% endhighlight %}

When using Kramdown code fences, line numbers are turned on globally by the
following configuration option:

{% highlight yaml %}
kramdown:
  syntax_highlighter_opts:
    block:
      line_numbers: true
{% endhighlight %}

Line numbers can then be suppressed locally using Liquid tags (_without_ the
`linenos` option) instead of fences:

{% highlight yaml %}
{% raw %}{% highlight some_language %}
Some code
{% endhighlight %}{% endraw %}
{% endhighlight %}

## Workarounds
{: .no_toc }
To use HTML compression together with line numbers, all highlighted code
needs to be wrapped using one of the following workarounds.
(The variable name `some_var` can be changed to avoid clashes; it can also
be replaced by `code` -- but note that `code=code` cannot be removed).

### Code fences (three backticks)
{: .no_toc }
{% highlight default %}
{% raw %}{% capture some_var %}
```some_language
Some code
```
{% endcapture %}
{% assign some_var = some_var | markdownify %}
{% include fix_linenos.html code=some_var %}{% endraw %}
{% endhighlight %}

### Liquid highlighting
{: .no_toc }
{% highlight default %}
{% raw %}{% capture some_var %}
{% highlight some_language linenos %}
Some code
{% endhighlight %}
{% endcapture %}
{% include fix_linenos.html code=some_var %}{% endraw %}
{% endhighlight %}

_Credit:_ The original version of the above workaround was suggested by
Dmitry Hrabrov at
<https://github.com/penibelst/jekyll-compress-html/issues/71#issuecomment-188144901>.

## Examples
{: .no_toc }
✅ Using code fences + workaround (will only show line numbers if enabled globally in `_config.yml`):

{% capture code_fence %}
```js
// Javascript code with syntax highlighting in fences
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```
{% endcapture %}
{% assign code_fence = code_fence | markdownify %}
{% include fix_linenos.html code=code_fence %}

✅ Using liquid highlighting + workaround:

{% capture code %}
{% highlight ruby linenos %}
### Ruby code with syntax highlighting and fixed line numbers using Liquid
{: .no_toc }
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
{% endhighlight %}
{% endcapture %}
{% include fix_linenos.html code=code %}
{% assign code = nil %}

❌ With the default configuration options, the following example illustrates
the **incorrect** formatting arising from the incompatibility of HTML compression
and the non-conforming HTML produced by Jekyll for line numbers:


# Lists

---

Most lists can be rendered with pure Markdown.

## Unordered list
{: .no_toc }
<div class="code-example" markdown="1">
- Item 1
- Item 2
- Item 3

_or_

* Item 1
* Item 2
* Item 3
</div>
```markdown
- Item 1
- Item 2
- Item 3

_or_

* Item 1
* Item 2
* Item 3
```

## Ordered list
{: .no_toc }
<div class="code-example" markdown="1">
1. Item 1
1. Item 2
1. Item 3
</div>
```markdown
1. Item 1
1. Item 2
1. Item 3
```

## Task list
{: .no_toc }
<div class="code-example" markdown="1">
- [ ] hello, this is a todo item
- [ ] hello, this is another todo item
- [x] goodbye, this item is done
</div>
```markdown
- [ ] hello, this is a todo item
- [ ] hello, this is another todo item
- [x] goodbye, this item is done
```

## Definition list
{: .no_toc }
Definition lists require HTML syntax and aren't supported with the GitHub Flavored Markdown compiler.

<div class="code-example" markdown="1">
<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>
</div>
```html
<dl>
  <dt>Name</dt>
  <dd>Godzilla</dd>
  <dt>Born</dt>
  <dd>1952</dd>
  <dt>Birthplace</dt>
  <dd>Japan</dd>
  <dt>Color</dt>
  <dd>Green</dd>
</dl>
```

# Responsive modifiers

Just the Docs spacing works in conjunction with a variety of modifiers that allow you to target specific screen sizes responsively. Use these in conjunction with spacing and display prefix and suffix classes.

| Modifier  | Screen size                          |
|:----------|:-------------------------------------|
| (none)    | All screens until the next modifier  |
| `xs`      | 320px (20rem) and up                 |
| `sm`      | 500px (31.25rem) and up              |
| `md`      | 740px (46.25rem) and up              |
| `lg`      | 1120px (70rem) and up                |
| `xl`      | 1400px (87.5rem) and up              |


# Tables

Tables are responsive by default, allowing wide tables to have a horizontal scroll to access columns outside of the normal viewport.

<div class="code-example" markdown="1">

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

</div>
```markdown
| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |
```
# Typography Utilities

---

## Font size
{: .no_toc }
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
{: .no_toc }
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
{: .no_toc }
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
{: .no_toc }
By default text is justified left. Use these `text-` classes to override settings:

| Class          | What it does         |
|:---------------|:---------------------|
| `.text-left`   | `text-align: left`   |
| `.text-right`  | `text-align: right`  |
| `.text-center` | `text-align: center` |


# Typography for UI Components

---

## Font stack
{: .no_toc }
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
{: .no_toc }
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

## Body text
{: .no_toc }
Default body text is rendered like this:

<div class="code-example" markdown="1">
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
</div>
```markdown
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
```

---

## Inline elements
{: .no_toc }
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
{: .no_toc }
There are a number of specific typographic CSS classes that allow you to override default styling for font size, font weight, line height, and capitalization.

[Original Link](https://github.com/pmarsceill/just-the-docs/blob/master/docs/index-test.md){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }