# HTML Text Elements

HTML text elements are used to display and format text on a webpage.

---

# 1. Headings (`<h1>` to `<h6>`)

HTML provides **6 levels of headings**.

* `<h1>` → Largest and most important heading
* `<h6>` → Smallest and least important heading

Example:

```html
<h1>Main Heading</h1>
<h2>Sub Heading</h2>
<h3>Section Heading</h3>
<h4>Small Heading</h4>
<h5>Smaller Heading</h5>
<h6>Smallest Heading</h6>
```

Output:

```
Main Heading
  Sub Heading
    Section Heading
      Small Heading
        Smaller Heading
          Smallest Heading
```

**Best Practice**

* Use only **one `<h1>`** per page.
* Follow a logical order (`h1 → h2 → h3`).

---

# 2. Paragraph (`<p>`)

Used to write paragraphs.

Example:

```html
<p>This is a paragraph.</p>

<p>HTML is easy to learn.</p>
```

---

# 3. Line Break (`<br>`)

Moves the text to the next line.

Example:

```html
<p>Hello<br>World</p>
```

Output:

```
Hello
World
```

`<br>` is an **empty (void) element**.

---

# 4. Horizontal Rule (`<hr>`)

Creates a horizontal line to separate content.

Example:

```html
<p>Chapter 1</p>

<hr>

<p>Chapter 2</p>
```

Output:

```
Chapter 1
----------------------
Chapter 2
```

---

# 5. Bold Text (`<b>`)

Displays text in **bold** without indicating extra importance.

Example:

```html
<p>This is <b>bold</b> text.</p>
```

Output:
**This is bold text.**

---

# 6. Strong Text (`<strong>`)

Displays text in bold and indicates that the content is **important**.

Example:

```html
<p><strong>Warning!</strong> Save your work.</p>
```

Output:
**Warning!** Save your work.

**Difference**

`<b>` → Bold appearance only.

`<strong>` → Bold + semantic importance.

---

# 7. Italic Text (`<i>`)

Displays text in italics for alternate voice or styling.

Example:

```html
<p>This is <i>italic</i> text.</p>
```

Output:
*This is italic text.*

---

# 8. Emphasized Text (`<em>`)

Indicates emphasis and is usually displayed in italics.

Example:

```html
<p>Please <em>read carefully</em>.</p>
```

Output:
Please *read carefully*.

**Difference**

`<i>` → Italic appearance only.

`<em>` → Italic + semantic emphasis.

---

# 9. Underlined Text (`<u>`)

Displays underlined text.

Example:

```html
<p>This is <u>underlined</u> text.</p>
```

Output:

This is <u>underlined</u> text.

---

# 10. Marked Text (`<mark>`)

Highlights text.

Example:

```html
<p>HTML is <mark>easy</mark> to learn.</p>
```

Output:

HTML is **highlighted** (usually with a yellow background).

---

# 11. Small Text (`<small>`)

Displays text in a smaller font.

Example:

```html
<p>This is normal text.</p>

<p><small>This is small text.</small></p>
```

---

# 12. Deleted Text (`<del>`)

Shows deleted text with a strikethrough.

Example:

```html
<p>Price: <del>$500</del> $300</p>
```

Output:

Price: ~~$500~~ $300

---

# 13. Inserted Text (`<ins>`)

Represents inserted text and is usually underlined.

Example:

```html
<p>I like <ins>HTML</ins>.</p>
```

---

# 14. Subscript (`<sub>`)

Displays text below the normal line.

Used for:

* Chemical formulas
* Mathematical notation

Example:

```html
<p>H<sub>2</sub>O</p>
```

Output:

H₂O

Another example:

```html
<p>CO<sub>2</sub></p>
```

Output:

CO₂

---

# 15. Superscript (`<sup>`)

Displays text above the normal line.

Used for:

* Exponents
* Ordinal numbers

Example:

```html
<p>2<sup>3</sup> = 8</p>
```

Output:

2³ = 8

Another example:

```html
<p>10<sup>th</sup></p>
```

Output:

10ᵗʰ

---

# 16. Preformatted Text (`<pre>`)

Preserves:

* Spaces
* Tabs
* Line breaks

Example:

```html
<pre>
Name : John
Age  : 22
City : Delhi
</pre>
```

Output:

```
Name : John
Age  : 22
City : Delhi
```

---

# 17. Code (`<code>`)

Displays computer code in a monospace font.

Example:

```html
<code>
console.log("Hello");
</code>
```

Output:

```
console.log("Hello");
```

---

# 18. Keyboard Input (`<kbd>`)

Represents keyboard input.

Example:

```html
<p>Press <kbd>Ctrl</kbd> + <kbd>S</kbd> to save.</p>
```

Output:

Press **Ctrl** + **S**

---

# 19. Variable (`<var>`)

Represents a variable in mathematics or programming.

Example:

```html
<p><var>x</var> = 10</p>
```

---

# 20. Sample Output (`<samp>`)

Represents output from a computer program.

Example:

```html
<p>Output: <samp>Hello World</samp></p>
```

---

# 21. Blockquote (`<blockquote>`)

Represents a long quotation.

Example:

```html
<blockquote>
The future depends on what you do today.
</blockquote>
```

Output:

> The future depends on what you do today.

---

# 22. Short Quotation (`<q>`)

Represents a short inline quotation.

Example:

```html
<p>He said, <q>Never give up.</q></p>
```

Output:

He said, "Never give up."

---

# 23. Abbreviation (`<abbr>`)

Shows the full form when hovered.

Example:

```html
<abbr title="HyperText Markup Language">HTML</abbr>
```

Output:

HTML *(hover to see "HyperText Markup Language")*

---

# 24. Address (`<address>`)

Represents contact information.

Example:

```html
<address>
John Doe<br>
Bengaluru<br>
India
</address>
```

---

# 25. Cite (`<cite>`)

Represents the title of a creative work (book, movie, painting, etc.).

Example:

```html
<p>My favorite book is <cite>The Alchemist</cite>.</p>
```

---

# 26. Bi-Directional Override (`<bdo>`)

Changes the direction of text.

Example:

```html
<bdo dir="rtl">Hello</bdo>
```

Output:

The word "Hello" is displayed from right to left.

---

# Summary Table

| Tag            | Purpose                  |
| -------------- | ------------------------ |
| `<h1>`–`<h6>`  | Headings                 |
| `<p>`          | Paragraph                |
| `<br>`         | Line break               |
| `<hr>`         | Horizontal line          |
| `<b>`          | Bold (styling only)      |
| `<strong>`     | Important text           |
| `<i>`          | Italic (styling only)    |
| `<em>`         | Emphasized text          |
| `<u>`          | Underlined text          |
| `<mark>`       | Highlighted text         |
| `<small>`      | Smaller text             |
| `<del>`        | Deleted text             |
| `<ins>`        | Inserted text            |
| `<sub>`        | Subscript                |
| `<sup>`        | Superscript              |
| `<pre>`        | Preformatted text        |
| `<code>`       | Code snippet             |
| `<kbd>`        | Keyboard input           |
| `<var>`        | Variable                 |
| `<samp>`       | Sample output            |
| `<blockquote>` | Long quotation           |
| `<q>`          | Inline quotation         |
| `<abbr>`       | Abbreviation             |
| `<address>`    | Contact information      |
| `<cite>`       | Title of a creative work |
| `<bdo>`        | Change text direction    |

---