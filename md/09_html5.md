# HTML5 Features

**HTML5** is the latest major version of HTML. It introduced **new semantic elements, multimedia support, improved forms, graphics APIs, storage, and many browser features** that make web development easier and more powerful.

---

# What is HTML5?

HTML5 is the fifth major version of HTML, officially released in **2014**.

It provides:

* Better page structure
* Native audio and video support
* New form controls
* Graphics support
* Local data storage
* Improved accessibility
* Better performance

---

# Major Features of HTML5

1. Semantic Elements
2. Native Audio
3. Native Video
4. Canvas
5. SVG
6. Improved Forms
7. Local Storage
8. Session Storage
9. Geolocation API
10. Drag and Drop API
11. Web Workers
12. Responsive Images
13. Custom Data Attributes
14. Improved Accessibility
15. New Input Types

---

# 1. Semantic Elements

Before HTML5:

```html id="17s1r3"
<div id="header"></div>

<div id="menu"></div>

<div id="content"></div>

<div id="footer"></div>
```

HTML5:

```html id="ycnw97"
<header></header>

<nav></nav>

<main></main>

<section></section>

<article></article>

<aside></aside>

<footer></footer>
```

### Benefits

* Better readability
* SEO-friendly
* Easier maintenance
* Improved accessibility

---

# 2. Native Audio Support

Before HTML5, playing audio required plugins.

HTML5 introduced:

```html id="h7np1l"
<audio controls>

<source src="song.mp3" type="audio/mpeg">

</audio>
```

Features:

* Play
* Pause
* Volume control
* Loop
* Autoplay
* Muted

---

# 3. Native Video Support

HTML5 can play videos without external plugins.

```html id="v1uikp"
<video controls width="500">

<source src="movie.mp4" type="video/mp4">

</video>
```

Supports:

* Play/Pause
* Fullscreen
* Poster image
* Subtitles (with `<track>`)
* Multiple video formats

---

# 4. Canvas (`<canvas>`)

Canvas allows drawing graphics using JavaScript.

Example:

```html id="b2x7d0"
<canvas
id="myCanvas"
width="300"
height="200">
</canvas>
```

Common Uses:

* Games
* Charts
* Animations
* Drawing apps
* Image editing

> **Note:** Canvas requires JavaScript to draw shapes and graphics.

---

# 5. SVG (Scalable Vector Graphics)

SVG creates vector graphics using XML.

Example:

```html id="jlwmz2"
<svg width="200" height="200">

<circle
cx="100"
cy="100"
r="50"
fill="red"/>

</svg>
```

Benefits:

* Scales without losing quality
* Small file size
* Easy to animate
* Great for icons and logos

---

# 6. Improved Forms

HTML5 introduced many new input types.

```html id="mlol40"
<input type="email">

<input type="date">

<input type="number">

<input type="color">

<input type="range">
```

Benefits:

* Built-in validation
* Better mobile keyboards
* Improved user experience

---

# 7. Local Storage

Stores data permanently in the browser.

JavaScript Example:

```javascript id="gydzt5"
localStorage.setItem("name", "John");

let name = localStorage.getItem("name");
```

Features:

* Data remains after closing the browser.
* Storage size is larger than cookies.
* Data is stored as key-value pairs.

---

# 8. Session Storage

Similar to Local Storage, but data is removed when the browser tab is closed.

```javascript id="gfjlwm"
sessionStorage.setItem("user", "Alice");
```

Difference:

| Local Storage            | Session Storage                |
| ------------------------ | ------------------------------ |
| Permanent                | Temporary                      |
| Survives browser restart | Cleared when tab/window closes |

---

# 9. Geolocation API

Gets the user's location (with permission).

Example (JavaScript):

```javascript id="7d3rww"
navigator.geolocation.getCurrentPosition(showPosition);
```

Uses:

* Maps
* Food delivery
* Ride-sharing apps
* Weather apps

---

# 10. Drag and Drop API

Allows users to drag and drop elements.

Common Uses:

* File uploads
* Reordering lists
* Dashboard widgets
* Kanban boards

---

# 11. Web Workers

Run JavaScript in the background without freezing the page.

Benefits:

* Better performance
* Smooth UI
* Background processing

Common Uses:

* Image processing
* Data calculations
* File conversions

---

# 12. Responsive Images

HTML5 works well with responsive web design.

Example:

```html id="yjlwmx"
<img
src="image.jpg"
alt="Nature"
style="max-width:100%; height:auto;">
```

Image automatically adjusts to screen size.

---

# 13. Custom Data Attributes

Store custom data inside HTML.

Example:

```html id="gwjlwm"
<div
data-id="101"
data-name="Laptop">
</div>
```

Access using JavaScript:

```javascript id="jlwmym"
element.dataset.id
```

---

# 14. Improved Accessibility

Semantic elements improve accessibility.

Example:

```html id="jlwmok"
<header>

<nav>

<main>

<footer>
```

Screen readers can better understand the page structure.

---

# 15. New Input Types

HTML5 introduced many useful input types.

```html id="jlwmph"
<input type="email">

<input type="url">

<input type="search">

<input type="tel">

<input type="date">

<input type="time">

<input type="month">

<input type="week">

<input type="datetime-local">

<input type="number">

<input type="range">

<input type="color">
```

---

# 16. New Form Attributes

HTML5 added useful attributes.

## Placeholder

```html id="jlwmpt"
<input
type="text"
placeholder="Enter Name">
```

---

## Required

```html id="jlwm9v"
<input
type="email"
required>
```

---

## Autofocus

```html id="jlwmzv"
<input
type="text"
autofocus>
```

Automatically focuses when the page loads.

---

## Pattern

```html id="jlwmpl"
<input
type="text"
pattern="[A-Za-z]{3,}">
```

Used for custom validation.

---

# 17. Progress Bar

Displays task progress.

```html id="jlwmgq"
<progress
value="60"
max="100">
</progress>
```

Output:

Progress: 60%

---

# 18. Meter

Represents a known measurement within a range.

Example:

```html id="jlwmli"
<meter
value="80"
min="0"
max="100">
</meter>
```

Common Uses:

* Disk usage
* Battery level
* Quiz score
* Download progress

---

# 19. Details and Summary

Creates expandable content.

```html id="jlwmg5"
<details>

<summary>Read More</summary>

<p>This is hidden content.</p>

</details>
```

---

# 20. Picture Element

Provides different images for different screen sizes.

```html id="jlwmkp"
<picture>

<source
media="(min-width:768px)"
srcset="large.jpg">

<img
src="small.jpg"
alt="Nature">

</picture>
```

Useful for responsive images.

---

# HTML4 vs HTML5

| HTML4                    | HTML5                                 |
| ------------------------ | ------------------------------------- |
| Plugin-based audio/video | Native audio/video                    |
| Mostly `<div>` layouts   | Semantic elements                     |
| Limited form controls    | Many new input types                  |
| No canvas                | Canvas support                        |
| No local storage         | Local & session storage               |
| Limited APIs             | Geolocation, Drag & Drop, Web Workers |
| Less accessible          | Better accessibility                  |

---

# Complete HTML5 Example

```html id="jlwm7u"
<!DOCTYPE html>
<html>
<head>
    <title>HTML5 Features</title>
</head>

<body>

<header>
    <h1>HTML5 Demo</h1>
</header>

<nav>
    <a href="#">Home</a>
</nav>

<main>

<section>

<h2>Audio</h2>

<audio controls>
    <source src="song.mp3" type="audio/mpeg">
</audio>

<h2>Video</h2>

<video controls width="400">
    <source src="movie.mp4" type="video/mp4">
</video>

<h2>Progress</h2>

<progress value="70" max="100"></progress>

<h2>Meter</h2>

<meter value="80" min="0" max="100"></meter>

<h2>Expandable Content</h2>

<details>

<summary>More Information</summary>

<p>HTML5 is powerful.</p>

</details>

</section>

</main>

<footer>

<p>© 2026 HTML5 Tutorial</p>

</footer>

</body>
</html>
```

---

# Best Practices

* Use semantic elements instead of generic `<div>`s when they describe the content.
* Use native `<audio>` and `<video>` elements instead of plugin-based solutions.
* Choose the appropriate HTML5 input type (`email`, `date`, `number`, etc.) for better validation and user experience.
* Add `alt` text to images and use semantic landmarks to improve accessibility.
* Use `<picture>` for responsive images when different image sources are needed for different screen sizes.
* Use browser storage (`localStorage` and `sessionStorage`) only for non-sensitive data. Never store passwords or confidential information in browser storage.

---

# Summary Table

| HTML5 Feature             | Purpose                              |
| ------------------------- | ------------------------------------ |
| Semantic Elements         | Meaningful page structure            |
| `<audio>`                 | Play audio                           |
| `<video>`                 | Play video                           |
| `<canvas>`                | Draw graphics with JavaScript        |
| `<svg>`                   | Scalable vector graphics             |
| New Input Types           | Better forms and validation          |
| Local Storage             | Persistent browser storage           |
| Session Storage           | Temporary browser storage            |
| Geolocation API           | Get user location                    |
| Drag and Drop API         | Drag-and-drop interactions           |
| Web Workers               | Background JavaScript processing     |
| `data-*` Attributes       | Store custom data in HTML            |
| `<progress>`              | Show task progress                   |
| `<meter>`                 | Display a measurement within a range |
| `<details>` / `<summary>` | Expandable content                   |
| `<picture>`               | Responsive images                    |

---
