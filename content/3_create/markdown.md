---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Formatting with Markdown

To effectively convey messages, a good design is indispensable. Even if your content is amazing, if it is presented as just a wall of plain text, chances are that people will not pay a lot of attention to it. 
Luckily, Jupyter Book has plenty of different options to format text, including media and much more.

On this page, we will review some basic Markdown formatting bits. For a more detailed view, check out [markdownguide.com](https://www.markdownguide.org/basic-syntax/) as one of many resources.


## Formatting Text

Let's start with the fundamentals:

### Headings

You can add headings using Markdown's syntax by adding `#` before your heading. You can vary the heading level by increasing the amount of Hash signs:
```
# Heading 1
## Heading 1.1
### Heading 1.1.1
```

### Italic
To make a text _italic_ add `_` or `*` before and after the word: 
|Syntax   | Output|
|---|---|
|`_italic_`| _italic_ |
|`*italic*` | *italic*|

### Bold
To make a text **bold** add `__` or `**` before and after the word: 

|Syntax   | Output|
|---|---|
|`__bold__`| __bold__ |
|`**bold**` | **bold**|

### (Nested) Lists
You can build nested itemized or enumerated lists using either `*` or `-` before a word:

```
* One
    - Sublist
        - This
    - Sublist
        - That
        - The other thing
```
Which results in:
* One
    - Sublist
        - This
    - Sublist
        - That
        - The other thing
    

You also create numbered lists by using `1.` etc. before your point:
```
1. Here we go
    1. Sublist
    2. Sublist
2. There we go
3. Now this
```
Which results in:

1. Here we go
    1. Sublist
    2. Sublist
2. There we go
3. Now this
  
### Horizontal Lines
You can add horizontal rules using three underscores `___` resulting in:

---

### Blockquotes
To create a blockquote, it is as simple as putting a `>` before a text.

Here is a blockquote:
```
> Beautiful is better than ugly.
> Explicit is better than implicit.
> Simple is better than complex.
> Complex is better than complicated.
```
And it's formatted like this: 
> Beautiful is better than ugly.
> Explicit is better than implicit.
> Simple is better than complex.
> Complex is better than complicated.


### Embedded Code

You can embed code meant for illustration instead of execution in Python by adding `` around statements:

```
`def f(x):`
` return x**2`
```
Which results in: 
`def f(x):`
` return x**2`

Since you need to add this line by line, this might ruin your code formatting. Instead, consider using the HTML formatting, adding `<code>` before and `</code>` after your code:
```
<code>def f(x): return x**2</code>
```
Which results in: 
<code>def f(x): return x**2</code>


### Writing Latex 

Let's use `%%` to render a block of `latex`:
|Syntax   | Output|
|---|---|
|`$$F(k) = \int_{-\infty}^{\infty} f(x) e^{2\pi i k} \mathrm{d} x$$`| $$F(k) = \int_{-\infty}^{\infty} f(x) e^{2\pi i k} \mathrm{d} x$$|


### Plotting in the Notebook

`Notebooks` support a variety of fantastic `plotting options`, including `static` and `interactive` graphics. This `magic` configures `matplotlib` to `render` its `figures` `inline`:

```{code-cell} python
%matplotlib inline
```

```{code-cell} python
import numpy as np
import matplotlib.pyplot as plt
```

```{code-cell} python
x = np.linspace(0, 2*np.pi, 300)
y = np.sin(x**2)
plt.plot(x, y)
plt.title("A little chirp")
fig = plt.gcf()  # let's keep the figure object around for later...
```


```{code-cell} python
import plotly.figure_factory as ff

# Add histogram data
x1 = np.random.randn(200) - 2
x2 = np.random.randn(200)
x3 = np.random.randn(200) + 2
x4 = np.random.randn(200) + 4

# Group data together
hist_data = [x1, x2, x3, x4]

group_labels = ['Group 1', 'Group 2', 'Group 3', 'Group 4']

# Create distplot with custom bin_size
fig = ff.create_distplot(hist_data, group_labels, bin_size=.2)
fig.show()
```

### Special Content Blocks - Directives and Roles
Directives and Roles are somewhat similiar to functions for markup language and allow for specific customizations of the look and feel of your book. Both accept various kinds of inputs, which are explained in further detail below.

#### Directives
With directives, you can adjust the look and feel of your Jupyter Book.

Directives are written like this:

```
```{mydirectivename}
My directive content
```

Where `{mydirectivename}`would be the name of the directive. However, this directive does not yet exist. While you can integrate directives, there are many directives already implemented in Jupyter Book. 
For instance, if you want to add a note, you can use:

```
```{note}
Here is a note
```
Which results in:
```{note}
Here is a note
```

#### Roles
 Roles are very similar in usage. However, they are somewhat simpler and are limited to one line.

 For example:
 ```
 Some content {rolename}`and here is my role's content!`
 ```
 
Where `{rolename}` would be the name of the role.

For instance, if you want to reference another page of your book, you can use the `{doc}`role:
```
{doc}`../1_github/intro`
``` 
Result: {doc}`../1_github/intro`.


#### What Roles and Directives Are Available?

For more information on what roles and directives you can use, check out:
* The [Sphinx directives page](https://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html) 
* The [reStructured Text directives page](https://docutils.sourceforge.io/docs/ref/rst/directives.html)
* For building [custom Special content blocks](https://jupyterbook.org/en/stable/content/content-blocks.html)


### Include Links

When adding links, you have several options. Here are the most common methods:

#### External Links
To link to an external website, use the following format: `[text](https://example.com)`

Example: `[Learn formatting with markdown](https://www.markdownguide.org/basic-syntax/)`

Result: [Learn formatting with markdown](https://www.markdownguide.org/basic-syntax/).

#### URL in New Tab
If you want the link to be opened in a new tab automatically, your can use the following HTML based format: `<a href="https://example.com" target="_blank">text</a>`

Example: `[Learn formatting with markdown](https://www.markdownguide.org/basic-syntax/){target="_blank"}`

Result: <a href="https://www.markdownguide.org/basic-syntax/" target="_blank">Learn formatting with markdown</a>.

#### Linking Another Page In Your Course
If you want to reference another file within your own project, use a relative path: `[text](relative_path)` 

When using relative paths, ../ is a special notation that tells the system to move up one level in the folder structure.

Example: `Check the [previous chapter](../2_host/host_website)`

Result: Check the [previous chapter](../2_host/host_website)

This method gives you full flexibility in how you phrase the link text. Alternatively, you can use the {doc} role, as explained above.

#### Direct URL
You can also display a URL as a clickable link without custom text by using angle brackets < >: `<URL>`

Example: `<https://www.markdownguide.org/basic-syntax/>`

Result: <https://www.markdownguide.org/basic-syntax/>

### Include Citations

In addition to linking external URLs, you can also include DOI links in your Markdown file. These will automatically be transformed into citations with a pop-up panel on hover, like this: [Cockett, 2022](https://doi.org/10.5281/zenodo.6476040). The full reference will then be added to the reference section at the bottom of your page. 

Example: `[Cockett, 2022](https://doi.org/10.5281/zenodo.6476040)`
Result: [Cockett, 2022](https://doi.org/10.5281/zenodo.6476040)


## Next Section:

In the next section, you will learn how to embed images, videos, and slides.




