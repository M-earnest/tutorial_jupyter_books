# Styling: The Look and Feel

To effectively convey messages, a good design is indispensable. Even if your content is amazing, if it is presented as just a wall of plain text, chances are that people will not pay a lot of attention to it. 
Luckily, Jupyter Book has plenty of different options to format text, including media and much more.

On this page, we will review some basic Markdown formatting bits. For a more detailed view, check out [markdownguide.com](https://www.markdownguide.org/basic-syntax/) as one of many resources.


### Formatting Text

Let's start with the fundamentals:

### Headings

You can add headings using Markdown's syntax by adding `#` before your heading. You can vary the heading level by increasing the amount of Hash signs:

<pre>
# Heading 1

# Heading 2

## Heading 2.1

## Heading 2.2
</pre>

#### Italic
To make a text _italic_ add `_` or `*` before and after the word: 
|Syntax   | Output|
|---|---|
|`_italic_`| _italic_ |
|`*italic*` | *italic*|

To make a text *bold* add "*" before and after the word: `*bold*`= *bold*

#### Bold
To make a text **bold** add `__` or `**` before and after the word: 

|Syntax   | Output|
|---|---|
|`__bold__`| __bold__ |
|`**bold**` | **bold**|


___
### (Nested) Lists
You can build nested itemized or enumerated lists using either `*` or `-` before a word

* One
    - Sublist
        - This
  - Sublist
        - That
        - The other thing
* Two
  - Sublist
* Three
  - Sublist

You also create numbered lists by using `1.` etc. before your point:

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

> Beautiful is better than ugly.
> Explicit is better than implicit.
> Simple is better than complex.
> Complex is better than complicated.


### Embedded code

You can embed code meant for illustration instead of execution in Python by adding `` before statements:

`def f(x):`

` return x**2`
Since you need to add this line by line, this might ruin your code formatting. Instead, consider using the HTML formatting, adding `<code>` before and `</code>` after your code:

<code>def f(x): return x**2</code>


### Writing latex 

Let's use `%%latex` to render a block of `latex`:
|Syntax   | Output|
|---|---|
|`$$F(k) = \int_{-\infty}^{\infty} f(x) e^{2\pi i k} \mathrm{d} x$$`| $$F(k) = \int_{-\infty}^{\infty} f(x) e^{2\pi i k} \mathrm{d} x$$|


### Plotting in the notebook

`Notebooks` support a variety of fantastic `plotting options`, including `static` and `interactive` graphics. This `magic` configures `matplotlib` to `render` its `figures` `inline`:

```python
    "%matplotlib inline"
```


