---
layout: default
title: Layout - List - Responsive
parent: Document Formatting
grand_parent: How To's
---

# Layout - List - Responsive
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

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
