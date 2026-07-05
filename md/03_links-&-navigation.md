# HTML Links and Navigation

Links are one of the most important features of HTML. They allow users to move from one webpage, website, section, email, or phone number to another.

---

# 1. HTML Link (`<a>` Tag)

The **anchor (`<a>`)** tag is used to create hyperlinks.

### Syntax

```html
<a href="URL">Link Text</a>
```

* `<a>` → Anchor tag
* `href` → Hypertext Reference (destination of the link)
* Link Text → Text visible to users

Example:

```html
<a href="https://www.google.com">Visit Google</a>
```

---

# 2. Absolute URL

An **absolute URL** points to another website.

Example:

```html
<a href="https://www.google.com">Google</a>

<a href="https://www.youtube.com">YouTube</a>
```

---

# 3. Relative URL

A **relative URL** points to another page within the same website.

Project Structure:

```
project/
│
├── index.html
├── about.html
├── contact.html
└── services.html
```

Example:

```html
<a href="about.html">About Us</a>

<a href="contact.html">Contact</a>

<a href="services.html">Services</a>
```

No need to write `https://`.

---

# 4. Opening Links in a New Tab

Use the `target` attribute.

```html
<a href="https://www.google.com" target="_blank">
    Open Google
</a>
```

### Common Values

| Value     | Description                 |
| --------- | --------------------------- |
| `_self`   | Opens in same tab (default) |
| `_blank`  | Opens in new tab            |
| `_parent` | Opens in parent frame       |
| `_top`    | Opens in full window        |

---

# 5. Security with `rel`

When using `target="_blank"`, it's good practice to add:

```html
<a href="https://example.com"
   target="_blank"
   rel="noopener noreferrer">
   Visit Website
</a>
```

**Why?**

* `noopener` prevents the new page from accessing your page through `window.opener`.
* `noreferrer` also prevents sending the referring page's URL.

---

# 6. Title Attribute

Shows a tooltip when hovering over the link.

```html
<a href="about.html" title="Go to About Page">
    About
</a>
```

---

# 7. Email Link

Use `mailto:`.

```html
<a href="mailto:john@example.com">
    Send Email
</a>
```

Clicking the link opens the default email application.

---

# 8. Phone Link

Use `tel:`.

```html
<a href="tel:+919876543210">
    Call Us
</a>
```

Useful for mobile devices.

---

# 9. Download Link

Use the `download` attribute.

```html
<a href="resume.pdf" download>
    Download Resume
</a>
```

The browser downloads the file instead of opening it (when supported).

---

# 10. Image as a Link

Images can also be clickable.

```html
<a href="index.html">
    <img src="logo.png" alt="Company Logo">
</a>
```

Clicking the image navigates to the homepage.

---

# 11. Linking to Sections (Bookmarks)

Navigate to a specific part of the same page.

### Step 1: Add an `id`

```html
<h2 id="contact">Contact Us</h2>
```

### Step 2: Create the link

```html
<a href="#contact">
    Go to Contact Section
</a>
```

---

# 12. Linking to a Section on Another Page

```html
<a href="about.html#team">
    Meet Our Team
</a>
```

---

# 13. Navigation Menu

A navigation menu is usually built using `<nav>`.

Example:

```html
<nav>
    <a href="index.html">Home</a> |
    <a href="about.html">About</a> |
    <a href="services.html">Services</a> |
    <a href="contact.html">Contact</a>
</nav>
```

---

# 14. Navigation Using Lists (Best Practice)

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

Using a list makes the navigation easier to style with CSS and improves accessibility.

---

# 15. Folder Navigation

Suppose your project is:

```
project/
│
├── index.html
├── about.html
│
├── pages/
│      contact.html
│      services.html
│
└── images/
       logo.png
```

### Open a file inside a folder

```html
<a href="pages/contact.html">Contact</a>
```

---

### Go back one folder

Suppose you're inside `pages/contact.html`.

```
project/
│
├── index.html
└── pages/
      contact.html
```

To open `index.html`:

```html
<a href="../index.html">Home</a>
```

`..` means **go up one directory**.

---

# 16. Multiple Folder Example

```
project/
│
├── index.html
│
├── pages/
│     services/
│          web.html
│
└── images/
      logo.png
```

From `web.html` to `index.html`:

```html
<a href="../../index.html">Home</a>
```

* First `..` → `services` → `pages`
* Second `..` → `pages` → `project`

---

# 17. Empty Link

Sometimes used as a placeholder.

```html
<a href="#">Click Here</a>
```

**Note:** Avoid using `#` as a final solution in production because it jumps to the top of the page.

---

# 18. JavaScript Link (Not Recommended for Navigation)

```html
<a href="javascript:void(0)">Do Nothing</a>
```

Use this only when appropriate; buttons are usually a better choice for actions.

---

# 19. Link States (CSS)

Links have four common states that can be styled with CSS:

```css
a:link {
    color: blue;
}

a:visited {
    color: purple;
}

a:hover {
    color: red;
}

a:active {
    color: green;
}
```

| State      | Description         |
| ---------- | ------------------- |
| `:link`    | Unvisited link      |
| `:visited` | Already visited     |
| `:hover`   | Mouse over the link |
| `:active`  | While being clicked |

---

# 20. Best Practices

* Use meaningful link text (e.g., **"Download Resume"** instead of **"Click Here"**).
* Use relative links for pages within your website.
* Use `target="_blank"` only when opening external websites or when appropriate.
* Add `rel="noopener noreferrer"` with `target="_blank"`.
* Use the `<nav>` element for navigation menus.
* Organize navigation with lists (`<ul>` and `<li>`).

---

# Mini Project Example

### Folder Structure

```
website/
│
├── index.html
├── about.html
├── services.html
├── contact.html
│
└── images/
      logo.png
```

### `index.html`

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
</head>
<body>

<nav>
    <a href="index.html">Home</a> |
    <a href="about.html">About</a> |
    <a href="services.html">Services</a> |
    <a href="contact.html">Contact</a>
</nav>

<h1>Welcome to My Website</h1>

<p>
    Learn more <a href="about.html">About Us</a>.
</p>

<p>
    Visit
    <a href="https://www.google.com"
       target="_blank"
       rel="noopener noreferrer">
       Google
    </a>
</p>

<p>
    <a href="mailto:info@example.com">Email Us</a>
</p>

<p>
    <a href="tel:+919876543210">Call Us</a>
</p>

</body>
</html>
```

---

# Summary Table

| Tag/Attribute               | Purpose                             |
| --------------------------- | ----------------------------------- |
| `<a>`                       | Create a hyperlink                  |
| `href`                      | Destination of the link             |
| `target="_blank"`           | Open in a new tab                   |
| `rel="noopener noreferrer"` | Improve security for new tabs       |
| `title`                     | Tooltip on hover                    |
| `mailto:`                   | Email link                          |
| `tel:`                      | Phone link                          |
| `download`                  | Download a file                     |
| `#id`                       | Link to a section on the same page  |
| `page.html#id`              | Link to a section on another page   |
| `<nav>`                     | Semantic navigation section         |
| `<ul><li>`                  | Best structure for navigation menus |
| `../`                       | Go up one folder                    |
| `../../`                    | Go up two folders                   |

---
