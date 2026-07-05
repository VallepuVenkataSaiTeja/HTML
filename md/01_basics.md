You're covering almost everything taught in **HTML Basics**. Here's a complete roadmap.

# HTML Basics

## 1. What is HTML?

* **HTML** = **HyperText Markup Language**
* It is the standard language used to create web pages.
* HTML defines the **structure** of a webpage.
* It is **not a programming language**; it is a **markup language**.

Example:

```html
<h1>Hello World</h1>
<p>This is my first webpage.</p>
```

---

## 2. History of HTML

| Version   | Year | Features                            |
| --------- | ---- | ----------------------------------- |
| HTML 1.0  | 1993 | Basic web pages                     |
| HTML 2.0  | 1995 | Standardized HTML                   |
| HTML 3.2  | 1997 | Tables, Applets                     |
| HTML 4.01 | 1999 | CSS support, Forms                  |
| XHTML     | 2000 | Stricter HTML rules                 |
| HTML5     | 2014 | Audio, Video, Canvas, Semantic Tags |

**Created by:** Tim Berners-Lee (1991)

---

## 3. HTML Document Structure

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Website</title>
</head>

<body>

    <h1>Hello World</h1>
    <p>Welcome to HTML</p>

</body>

</html>
```

### Explanation

### `<!DOCTYPE html>`

Tells the browser that the document uses HTML5.

### `<html>`

Root element of the webpage.

### `<head>`

Contains metadata like:

* Title
* CSS links
* Meta tags
* Icons

### `<body>`

Contains everything visible on the webpage.

---

## 4. HTML Comments

Used to write notes that browsers ignore.

```html
<!-- This is a comment -->
```

Shortcut:

```
Ctrl + /
```

Example:

```html
<!-- Header Section -->
<h1>Welcome</h1>
```

---

# 5. VS Code Shortcuts

| Shortcut           | Purpose               |
| ------------------ | --------------------- |
| Ctrl + /           | Comment line          |
| Shift + Alt + Down | Duplicate line        |
| Alt + Up/Down      | Move line             |
| Ctrl + D           | Select next same word |
| Ctrl + Shift + K   | Delete line           |
| Ctrl + Space       | Trigger suggestions   |
| Ctrl + Shift + P   | Command Palette       |
| Ctrl + S           | Save                  |
| Ctrl + Z           | Undo                  |
| Ctrl + Y           | Redo                  |
| Ctrl + F           | Find                  |
| Ctrl + H           | Replace               |
| Alt + Click        | Multiple cursors      |
| Ctrl + `           | Open Terminal         |

---

# 6. Emmet

Emmet is a shortcut system that generates HTML quickly.

Example:

Type

```text
!
```

Press **Tab**

Output:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

</body>
</html>
```

---

### Common Emmet Examples

#### Heading

```text
h1
```

↓

```html
<h1></h1>
```

---

#### Paragraph

```text
p
```

↓

```html
<p></p>
```

---

#### Multiple Tags

```text
li*5
```

↓

```html
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
```

---

#### Parent with Child

```text
ul>li
```

↓

```html
<ul>
    <li></li>
</ul>
```

---

#### Siblings

```text
h1+p
```

↓

```html
<h1></h1>
<p></p>
```

---

#### Class

```text
div.container
```

↓

```html
<div class="container"></div>
```

---

#### ID

```text
div#header
```

↓

```html
<div id="header"></div>
```

---

#### Class + Child

```text
nav>ul>li*4
```

↓

```html
<nav>
    <ul>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
    </ul>
</nav>
```

---

#### Text

```text
p{Hello World}
```

↓

```html
<p>Hello World</p>
```

---

#### Numbering

```text
ul>li.item$*5
```

↓

```html
<ul>
    <li class="item1"></li>
    <li class="item2"></li>
    <li class="item3"></li>
    <li class="item4"></li>
    <li class="item5"></li>
</ul>
```

---

# 7. File Extension

HTML files are saved with:

```text
.html
```

Example:

```
index.html
about.html
contact.html
```

---

# 8. HTML Elements

An HTML element usually consists of:

```html
<tag>Content</tag>
```

Example:

```html
<p>Hello</p>
```

* Opening tag: `<p>`
* Content: `Hello`
* Closing tag: `</p>`

---

# 9. HTML Tags

Tags tell the browser what type of content to display.

Examples:

```html
<h1></h1>
<p></p>
<img>
<a></a>
<div></div>
```

---

# 10. Attributes

Attributes provide extra information about an element.

Example:

```html
<a href="https://example.com">Visit</a>
```

Here:

* Tag → `a`
* Attribute → `href`

Another example:

```html
<img src="image.jpg" alt="Flower">
```

---

# 11. Empty (Void) Elements

These do **not** have closing tags.

Examples:

```html
<br>
<hr>
<img>
<input>
<meta>
<link>
```

---

# 12. Nesting

HTML elements can be placed inside other elements.

```html
<div>
    <h1>Welcome</h1>
    <p>Hello</p>
</div>
```

---

# 13. Case Sensitivity

HTML tags are **not case-sensitive**, but the convention is to write them in **lowercase**.

✔️ Recommended:

```html
<h1>Hello</h1>
```

❌ Avoid:

```html
<H1>Hello</H1>
```

---

# 14. Indentation

Proper indentation improves readability.

✔️ Good:

```html
<body>
    <h1>Hello</h1>
</body>
```

---

# 15. Browser Inspection

Useful tools:

* **Inspect Element** (Developer Tools)
* **View Page Source**

Shortcut:

```
F12
```

or

```
Ctrl + Shift + I
```

---