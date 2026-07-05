# HTML Lists

Lists are used to organize related items in a structured way. HTML provides **three types of lists**:

1. **Ordered List (`<ol>`)** – Numbered list
2. **Unordered List (`<ul>`)** – Bulleted list
3. **Description List (`<dl>`)** – Terms and their descriptions

---

# 1. Ordered List (`<ol>`)

An ordered list displays items in a numbered sequence.

## Syntax

```html
<ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ol>
```

### Output

```text
1. Item 1
2. Item 2
3. Item 3
```

---

# 2. List Item (`<li>`)

The `<li>` (List Item) tag defines each item inside an ordered or unordered list.

Example:

```html
<ol>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ol>
```

---

# 3. Unordered List (`<ul>`)

An unordered list displays items using bullets.

## Syntax

```html
<ul>
    <li>Apple</li>
    <li>Mango</li>
    <li>Orange</li>
</ul>
```

### Output

```text
• Apple
• Mango
• Orange
```

---

# 4. Ordered List Types

Use the `type` attribute to change numbering style.

## Numbers (Default)

```html
<ol type="1">
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ol>
```

Output:

```text
1. HTML
2. CSS
3. JavaScript
```

---

## Uppercase Letters

```html
<ol type="A">
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ol>
```

Output:

```text
A. HTML
B. CSS
C. JavaScript
```

---

## Lowercase Letters

```html
<ol type="a">
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ol>
```

Output:

```text
a. HTML
b. CSS
c. JavaScript
```

---

## Uppercase Roman Numbers

```html
<ol type="I">
    <li>Chapter One</li>
    <li>Chapter Two</li>
</ol>
```

Output:

```text
I. Chapter One
II. Chapter Two
```

---

## Lowercase Roman Numbers

```html
<ol type="i">
    <li>Chapter One</li>
    <li>Chapter Two</li>
</ol>
```

Output:

```text
i. Chapter One
ii. Chapter Two
```

---

# 5. Start Attribute

Starts numbering from a specific value.

Example:

```html
<ol start="5">
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ol>
```

Output:

```text
5. HTML
6. CSS
7. JavaScript
```

---

# 6. Reversed Ordered List

Displays numbering in reverse order.

```html
<ol reversed>
    <li>Third</li>
    <li>Second</li>
    <li>First</li>
</ol>
```

Output:

```text
3. Third
2. Second
1. First
```

---

# 7. List Item Value

Set the number for a particular list item.

```html
<ol>
    <li>HTML</li>
    <li value="10">CSS</li>
    <li>JavaScript</li>
</ol>
```

Output:

```text
1. HTML
10. CSS
11. JavaScript
```

---

# 8. Unordered List Styles

The `type` attribute for `<ul>` is obsolete in HTML5. Use CSS instead.

Example:

```html
<ul style="list-style-type: square;">
    <li>Apple</li>
    <li>Mango</li>
</ul>
```

Common values:

```css
list-style-type: disc;
list-style-type: circle;
list-style-type: square;
list-style-type: none;
```

---

# 9. Nested Lists

Lists can be placed inside other lists.

Example:

```html
<ul>
    <li>Frontend
        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
        </ul>
    </li>

    <li>Backend</li>
</ul>
```

Output:

```text
• Frontend
   • HTML
   • CSS
   • JavaScript

• Backend
```

---

# 10. Mixed Lists

You can combine ordered and unordered lists.

```html
<ol>
    <li>Frontend
        <ul>
            <li>HTML</li>
            <li>CSS</li>
        </ul>
    </li>

    <li>Backend</li>
</ol>
```

Output:

```text
1. Frontend
    • HTML
    • CSS

2. Backend
```

---

# 11. Description List (`<dl>`)

Used for terms and their descriptions.

### Tags Used

* `<dl>` → Description List
* `<dt>` → Description Term
* `<dd>` → Description Details

Example:

```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>

    <dt>CSS</dt>
    <dd>Cascading Style Sheets</dd>

    <dt>JavaScript</dt>
    <dd>Programming language for web pages.</dd>
</dl>
```

Output:

```text
HTML
   HyperText Markup Language

CSS
   Cascading Style Sheets

JavaScript
   Programming language for web pages.
```

---

# 12. Navigation Menu Using Lists

Lists are commonly used to create website navigation.

```html
<nav>
    <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="services.html">Services</a></li>
        <li><a href="contact.html">Contact</a></li>
    </ul>
</nav>
```

---

# 13. Horizontal Navigation (with CSS)

```html
<ul>
    <li>Home</li>
    <li>About</li>
    <li>Contact</li>
</ul>
```

```css
ul {
    list-style: none;
}

li {
    display: inline;
    margin-right: 20px;
}
```

Output:

```text
Home   About   Contact
```

---

# 14. Common Use Cases

### Ordered List

* Step-by-step instructions
* Rankings
* Recipes
* Procedures

Example:

```html
<ol>
    <li>Open VS Code</li>
    <li>Create index.html</li>
    <li>Run in Browser</li>
</ol>
```

---

### Unordered List

* Menu items
* Features
* Categories
* Shopping lists

Example:

```html
<ul>
    <li>Milk</li>
    <li>Bread</li>
    <li>Eggs</li>
</ul>
```

---

### Description List

* Glossary
* Dictionary
* FAQs
* Product specifications

Example:

```html
<dl>
    <dt>CPU</dt>
    <dd>Central Processing Unit</dd>
</dl>
```

---

# Best Practices

* Use `<ol>` when the order of items matters.
* Use `<ul>` when the order does not matter.
* Use `<dl>` for terms and definitions.
* Always place `<li>` elements inside `<ol>` or `<ul>`.
* Use CSS to style list markers instead of the obsolete `type` attribute on `<ul>`.

---

# Mini Project Example

```html
<!DOCTYPE html>
<html>
<head>
    <title>HTML Lists</title>
</head>
<body>

<h1>HTML Lists</h1>

<h2>Ordered List</h2>

<ol>
    <li>Wake Up</li>
    <li>Exercise</li>
    <li>Study HTML</li>
</ol>

<h2>Unordered List</h2>

<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>

<h2>Nested List</h2>

<ul>
    <li>Frontend
        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
        </ul>
    </li>

    <li>Backend</li>
</ul>

<h2>Description List</h2>

<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>

    <dt>CSS</dt>
    <dd>Cascading Style Sheets</dd>
</dl>

</body>
</html>
```

---

# Summary Table

| Tag/Attribute           | Purpose                                   |
| ----------------------- | ----------------------------------------- |
| `<ol>`                  | Ordered (numbered) list                   |
| `<ul>`                  | Unordered (bulleted) list                 |
| `<li>`                  | List item                                 |
| `<dl>`                  | Description list                          |
| `<dt>`                  | Description term                          |
| `<dd>`                  | Description/details                       |
| `type` (on `<ol>`)      | Numbering style (`1`, `A`, `a`, `I`, `i`) |
| `start`                 | Start numbering from a specific value     |
| `reversed`              | Reverse the numbering order               |
| `value`                 | Set the value of a specific list item     |
| `list-style-type` (CSS) | Change bullet style                       |

---