# Semantic HTML

Semantic HTML uses elements that **describe the meaning and purpose of the content**, making web pages easier for developers, browsers, search engines, and assistive technologies to understand.

Instead of using generic elements like `<div>` and `<span>` everywhere, semantic HTML provides meaningful tags such as `<header>`, `<nav>`, `<main>`, and `<footer>`.

---

# 1. What is Semantic HTML?

**Semantic** means **meaningful**.

### Non-Semantic HTML

```html id="spplpr"
<div id="header">
    <h1>My Website</h1>
</div>

<div id="menu">
    Home | About | Contact
</div>

<div id="content">
    Welcome to my website.
</div>

<div id="footer">
    Copyright 2026
</div>
```

The browser doesn't know what each `<div>` represents.

---

### Semantic HTML

```html id="pm6jlwm"
<header>
    <h1>My Website</h1>
</header>

<nav>
    Home | About | Contact
</nav>

<main>
    Welcome to my website.
</main>

<footer>
    Copyright 2026
</footer>
```

Now the structure is clear and meaningful.

---

# 2. Why Use Semantic HTML?

### Advantages

* Better code readability.
* Improves accessibility.
* Helps search engines understand your page (SEO).
* Easier to maintain.
* Creates a logical document structure.

---

# 3. Page Structure

A typical semantic HTML page looks like this:

```text id="xg0gdw"
+----------------------------------+
| Header                           |
+----------------------------------+
| Navigation                       |
+----------------------------------+
| Main                             |
|  +----------------------------+  |
|  | Section                    |  |
|  |   Article                  |  |
|  +----------------------------+  |
|  | Aside                      |  |
|  +----------------------------+  |
+----------------------------------+
| Footer                           |
+----------------------------------+
```

---

# 4. `<header>`

Represents introductory content.

Usually contains:

* Logo
* Website title
* Search bar
* Navigation (sometimes)

Example:

```html id="txr3fd"
<header>
    <h1>Tech World</h1>
    <p>Learn Web Development</p>
</header>
```

A page or an individual `<article>` can have its own `<header>`.

---

# 5. `<nav>`

Represents navigation links.

Example:

```html id="7o30d2"
<nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="contact.html">Contact</a>
</nav>
```

Usually contains:

* Main menu
* Sidebar navigation
* Table of contents

---

# 6. `<main>`

Represents the main content of the page.

Rules:

* Only **one `<main>`** per page.
* Should not contain repeated content like headers or footers.

Example:

```html id="y9hkrv"
<main>

<h2>Latest Articles</h2>

<p>Welcome to our blog.</p>

</main>
```

---

# 7. `<section>`

Represents a thematic group of related content.

Example:

```html id="w2h9ij"
<section>

<h2>Our Courses</h2>

<p>HTML</p>

<p>CSS</p>

<p>JavaScript</p>

</section>
```

Use `<section>` when the content has a heading and forms a logical part of the page.

---

# 8. `<article>`

Represents independent, self-contained content.

Examples:

* Blog post
* News article
* Forum post
* Product review
* User comment

Example:

```html id="5qexy4"
<article>

<h2>HTML Basics</h2>

<p>HTML is the standard markup language...</p>

</article>
```

An `<article>` should make sense even if viewed by itself.

---

# 9. `<aside>`

Represents content related to, but separate from, the main content.

Examples:

* Sidebar
* Advertisements
* Related posts
* Author information
* Quick links

Example:

```html id="phyy2x"
<aside>

<h3>Related Articles</h3>

<ul>

<li>CSS Basics</li>

<li>JavaScript Basics</li>

</ul>

</aside>
```

---

# 10. `<footer>`

Represents the footer.

Usually contains:

* Copyright
* Contact details
* Social media links
* Privacy Policy
* Terms of Service

Example:

```html id="5axg57"
<footer>

<p>© 2026 My Website</p>

</footer>
```

A page or an `<article>` can have its own footer.

---

# 11. `<figure>`

Represents self-contained media.

Example:

```html id="gn5lym"
<figure>

<img src="mountain.jpg" alt="Mountain">

<figcaption>Beautiful Mountain</figcaption>

</figure>
```

---

# 12. `<figcaption>`

Provides a caption for a figure.

Example:

```html id="wnz8lm"
<figure>

<img src="flower.jpg" alt="Flower">

<figcaption>Red Rose</figcaption>

</figure>
```

---

# 13. `<details>`

Creates expandable content.

Example:

```html id="7ntjlwm"
<details>

<summary>Read More</summary>

<p>This is hidden content.</p>

</details>
```

Output:

▶ Read More

When clicked:

▼ Read More

This is hidden content.

---

# 14. `<summary>`

Defines the visible heading inside `<details>`.

Example:

```html id="3g0xys"
<details>

<summary>Course Details</summary>

<p>Duration: 3 Months</p>

</details>
```

---

# 15. `<time>`

Represents dates and times.

Example:

```html id="jqe5yr"
<p>

Published on

<time datetime="2026-07-03">

July 3, 2026

</time>

</p>
```

`datetime` provides a machine-readable value.

---

# 16. `<mark>`

Highlights text.

```html id="8c39zc"
<p>

HTML is

<mark>easy</mark>

to learn.

</p>
```

---

# 17. `<address>`

Represents contact information.

```html id="9q6vpg"
<address>

ABC Company

<br>

Bengaluru

<br>

India

</address>
```

---

# 18. Semantic vs Non-Semantic Elements

## Semantic Elements

| Tag            | Purpose                 |
| -------------- | ----------------------- |
| `<header>`     | Introductory content    |
| `<nav>`        | Navigation              |
| `<main>`       | Main page content       |
| `<section>`    | Related content section |
| `<article>`    | Independent content     |
| `<aside>`      | Sidebar/related content |
| `<footer>`     | Footer                  |
| `<figure>`     | Self-contained media    |
| `<figcaption>` | Caption for a figure    |
| `<details>`    | Expandable content      |
| `<summary>`    | Heading for details     |
| `<time>`       | Date/time               |
| `<address>`    | Contact information     |

---

## Non-Semantic Elements

| Tag      | Purpose                  |
| -------- | ------------------------ |
| `<div>`  | Generic block container  |
| `<span>` | Generic inline container |

They don't describe the purpose of the content.

---

# 19. Complete Page Example

```html id="jlwmcv"
<!DOCTYPE html>
<html>
<head>
    <title>Semantic HTML</title>
</head>

<body>

<header>

<h1>My Blog</h1>

</header>

<nav>

<a href="#">Home</a>

<a href="#">Articles</a>

<a href="#">Contact</a>

</nav>

<main>

<section>

<h2>Latest Articles</h2>

<article>

<h3>HTML Basics</h3>

<p>Learn HTML from scratch.</p>

<footer>

Published by John

</footer>

</article>

</section>

<aside>

<h3>Popular Posts</h3>

<ul>

<li>CSS</li>

<li>JavaScript</li>

</ul>

</aside>

</main>

<footer>

<p>© 2026 My Blog</p>

</footer>

</body>

</html>
```

---

# Semantic Page Layout

```text id="d9aq5i"
<body>
│
├── <header>
│
├── <nav>
│
├── <main>
│     │
│     ├── <section>
│     │      │
│     │      └── <article>
│     │
│     └── <aside>
│
└── <footer>
```

---

# Best Practices

* Use **one `<main>`** element per page.
* Use `<header>` and `<footer>` for introductory and ending content.
* Use `<nav>` only for major navigation links.
* Use `<section>` for related content with a heading.
* Use `<article>` for standalone content that can be reused or shared.
* Use `<aside>` for related but secondary content.
* Use `<figure>` with `<figcaption>` for images, diagrams, or code examples with captions.
* Don't replace every `<div>` with a semantic tag—use semantic elements only when they accurately describe the content.

---

# Summary Table

| Semantic Tag   | Purpose                                 |
| -------------- | --------------------------------------- |
| `<header>`     | Introductory content                    |
| `<nav>`        | Navigation links                        |
| `<main>`       | Main content                            |
| `<section>`    | Thematic section                        |
| `<article>`    | Independent content                     |
| `<aside>`      | Sidebar/related content                 |
| `<footer>`     | Footer                                  |
| `<figure>`     | Self-contained media                    |
| `<figcaption>` | Figure caption                          |
| `<details>`    | Expandable content                      |
| `<summary>`    | Title for `<details>`                   |
| `<time>`       | Date and time                           |
| `<mark>`       | Highlighted text                        |
| `<address>`    | Contact information                     |
| `<div>`        | Generic block container (non-semantic)  |
| `<span>`       | Generic inline container (non-semantic) |

---