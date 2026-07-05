# HTML Accessibility (a11y)

**Accessibility** means designing websites so that **everyone**, including people with disabilities, can use them effectively.

The term **a11y** comes from:

* **a** + **11 letters** + **y** = **accessibility**

Accessibility helps users who:

* Have visual impairments
* Have hearing impairments
* Have motor disabilities
* Have cognitive disabilities
* Use keyboards instead of a mouse
* Use screen readers or other assistive technologies

---

# 1. Why is Accessibility Important?

### Benefits

* Makes websites usable for everyone.
* Improves SEO (Search Engine Optimization).
* Enhances user experience.
* Helps meet legal and organizational accessibility standards.
* Makes websites easier to maintain.

---

# 2. Use Semantic HTML

Semantic elements help browsers and assistive technologies understand the page structure.

❌ Non-semantic

```html
<div id="header">
    Welcome
</div>

<div id="footer">
    Copyright
</div>
```

✅ Semantic

```html
<header>
    Welcome
</header>

<footer>
    Copyright
</footer>
```

Common semantic elements:

* `<header>`
* `<nav>`
* `<main>`
* `<section>`
* `<article>`
* `<aside>`
* `<footer>`

---

# 3. Add `alt` Text to Images

Every meaningful image should have an `alt` attribute.

Good example:

```html
<img src="flower.jpg"
     alt="Red rose in a garden">
```

Decorative image:

```html
<img src="border.png"
     alt="">
```

### Good `alt` Text

✔️ Describe the image briefly.

```html
alt="Student writing HTML code"
```

### Bad `alt` Text

```html
alt="image"
```

or

```html
alt="photo123"
```

---

# 4. Use Labels with Form Controls

❌ Bad

```html
<input type="text">
```

✅ Good

```html
<label for="name">Name</label>

<input
type="text"
id="name">
```

Clicking the label focuses the input, making forms easier to use.

---

# 5. Keyboard Accessibility

Many users navigate using only the keyboard.

Users should be able to:

* Tab through links
* Access buttons
* Fill forms
* Open menus

Useful keys:

| Key         | Purpose                          |
| ----------- | -------------------------------- |
| Tab         | Move forward                     |
| Shift + Tab | Move backward                    |
| Enter       | Activate button/link             |
| Space       | Select checkbox/button           |
| Arrow Keys  | Navigate menus and radio buttons |

---

# 6. Use Proper Heading Order

Correct:

```html
<h1>Website</h1>

<h2>Courses</h2>

<h3>HTML</h3>
```

Incorrect:

```html
<h1>Website</h1>

<h4>HTML</h4>
```

Avoid skipping heading levels.

---

# 7. Use Descriptive Link Text

❌ Bad

```html
<a href="course.html">

Click Here

</a>
```

✅ Good

```html
<a href="course.html">

Learn HTML Basics

</a>
```

Users should understand the destination without additional context.

---

# 8. Provide Captions for Videos

Videos should include captions.

Example:

```html
<video controls>

<source src="video.mp4">

</video>
```

Provide:

* Captions
* Subtitles
* Transcripts when possible

This helps users who are deaf or hard of hearing.

---

# 9. Audio Transcripts

Audio-only content should provide text transcripts.

Example:

Podcast

↓

Transcript

This helps users who cannot hear the audio.

---

# 10. Use Buttons for Actions

❌ Wrong

```html
<a href="#"
onclick="submitForm()">

Submit

</a>
```

✅ Correct

```html
<button type="submit">

Submit

</button>
```

* Use `<a>` for navigation.
* Use `<button>` for actions.

---

# 11. Use Tables Properly

Always use table headers.

```html
<table>

<tr>

<th>Name</th>

<th>Age</th>

</tr>

<tr>

<td>John</td>

<td>22</td>

</tr>

</table>
```

Do not use tables for page layout.

---

# 12. Use Language Attribute

Always specify the page language.

```html
<html lang="en">
```

Examples:

```html
<html lang="en">
```

```html
<html lang="fr">
```

```html
<html lang="hi">
```

This helps screen readers pronounce text correctly.

---

# 13. Color Contrast

Ensure text is easy to read.

❌ Poor contrast

Light gray text on a white background.

✅ Good contrast

Black text on a white background.

Example:

```css
body {

color: black;

background: white;

}
```

---

# 14. Don't Rely Only on Color

❌ Wrong

```text
Red = Error
Green = Success
```

✅ Better

```text
❌ Error

✔ Success
```

Or combine color with icons or text labels.

---

# 15. Focus Indicators

Keyboard users need to know which element is currently selected.

Default browser focus:

```css
button:focus {

outline: auto;

}
```

Avoid removing outlines unless you provide an equally visible replacement.

---

# 16. ARIA (Accessible Rich Internet Applications)

ARIA improves accessibility for dynamic interfaces.

Example:

```html
<button
aria-label="Close">

×

</button>
```

Useful ARIA attributes:

| Attribute       | Purpose                    |
| --------------- | -------------------------- |
| `aria-label`    | Accessible label           |
| `aria-hidden`   | Hide from screen readers   |
| `aria-expanded` | Expanded/collapsed state   |
| `aria-live`     | Announce dynamic updates   |
| `role`          | Defines the element's role |

Use ARIA **only when native HTML cannot provide the required accessibility**.

---

# 17. Screen Readers

Screen readers convert webpage content into speech or Braille.

They rely on:

* Headings
* Labels
* Alt text
* Semantic HTML
* ARIA (when appropriate)

---

# 18. Skip Navigation Link

Allows keyboard users to jump directly to the main content.

```html
<a href="#main">

Skip to Main Content

</a>

<main id="main">

...

</main>
```

---

# 19. Responsive Design

Accessibility also includes usability on different devices.

Use:

```html
<meta
name="viewport"
content="width=device-width, initial-scale=1.0">
```

And responsive CSS.

---

# 20. Accessible Form Example

```html
<form>

<label for="name">

Name

</label>

<input
type="text"
id="name"
required>

<br><br>

<label for="email">

Email

</label>

<input
type="email"
id="email"
required>

<br><br>

<button
type="submit">

Register

</button>

</form>
```

---

# 21. Accessible Navigation

```html
<nav>

<ul>

<li>

<a href="index.html">

Home

</a>

</li>

<li>

<a href="about.html">

About

</a>

</li>

<li>

<a href="contact.html">

Contact

</a>

</li>

</ul>

</nav>
```

---

# 22. Accessibility Checklist

* ✅ Use semantic HTML.
* ✅ Add `alt` text to meaningful images.
* ✅ Associate labels with form controls.
* ✅ Use headings in the correct order.
* ✅ Make the site keyboard accessible.
* ✅ Use descriptive link text.
* ✅ Add captions and transcripts for media.
* ✅ Ensure sufficient color contrast.
* ✅ Don't rely only on color.
* ✅ Keep focus indicators visible.
* ✅ Specify the page language (`lang`).
* ✅ Use buttons for actions and links for navigation.
* ✅ Use ARIA only when necessary.
* ✅ Test with keyboard navigation and screen readers.

---

# Complete Accessible HTML Example

```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta
name="viewport"
content="width=device-width, initial-scale=1.0">

<title>Accessible Page</title>

</head>

<body>

<a href="#main">

Skip to Main Content

</a>

<header>

<h1>HTML Accessibility</h1>

</header>

<nav>

<ul>

<li><a href="#">Home</a></li>

<li><a href="#">About</a></li>

<li><a href="#">Contact</a></li>

</ul>

</nav>

<main id="main">

<img
src="student.jpg"
alt="Student learning HTML">

<form>

<label for="email">

Email

</label>

<input
type="email"
id="email"
required>

<br><br>

<button
type="submit">

Submit

</button>

</form>

</main>

<footer>

<p>© 2026</p>

</footer>

</body>

</html>
```

---

# Best Practices

* Prefer **native HTML elements** (`<button>`, `<label>`, `<nav>`, etc.) over custom components whenever possible.
* Write meaningful `alt` text for informative images and use `alt=""` for decorative images.
* Use headings in a logical hierarchy (`<h1>` → `<h2>` → `<h3>`).
* Ensure all interactive elements are usable with a keyboard.
* Provide captions for videos and transcripts for audio.
* Maintain sufficient color contrast and don't rely on color alone to communicate information.
* Use ARIA only to enhance accessibility when native HTML is not enough.

---

# Summary Table

| Feature                | Purpose                             |
| ---------------------- | ----------------------------------- |
| Semantic HTML          | Meaningful page structure           |
| `alt`                  | Image description                   |
| `<label>`              | Form accessibility                  |
| Heading hierarchy      | Better navigation                   |
| Keyboard support       | Access without a mouse              |
| Descriptive links      | Clear navigation                    |
| Captions & transcripts | Accessible media                    |
| `lang`                 | Language for screen readers         |
| Color contrast         | Readable content                    |
| Focus indicators       | Visible keyboard focus              |
| ARIA                   | Improve accessibility for custom UI |
| Skip link              | Jump to main content                |

---