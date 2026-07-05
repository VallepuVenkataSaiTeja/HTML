# HTML Forms

HTML forms are used to **collect user input**. They are commonly used for:

* User Registration
* Login
* Contact Forms
* Feedback Forms
* Surveys
* Search Boxes
* Payment Details

---

# 1. What is a Form?

A form is created using the `<form>` element.

## Syntax

```html
<form>
    <!-- Form elements go here -->
</form>
```

Example:

```html
<form>
    <input type="text">
</form>
```

---

# 2. The `<form>` Tag

The `<form>` element acts as a container for all form controls.

### Syntax

```html
<form action="submit.php" method="post">

</form>
```

### Common Attributes

| Attribute      | Purpose                       |
| -------------- | ----------------------------- |
| `action`       | URL where form data is sent   |
| `method`       | HTTP method (`GET` or `POST`) |
| `autocomplete` | Enable/disable autocomplete   |
| `target`       | Where to display the response |
| `novalidate`   | Disable browser validation    |

Example:

```html
<form action="login.php" method="post">

</form>
```

---

# 3. Form Methods

## GET

* Data is sent through the URL.
* Suitable for searches and filters.
* Less secure for sensitive information.

Example:

```html
<form action="/search" method="get">
```

URL Example:

```text
/search?name=John
```

---

## POST

* Data is sent in the request body.
* More secure than GET.
* Used for login, registration, and payments.

Example:

```html
<form action="/register" method="post">
```

---

# 4. `<label>`

Labels describe form fields.

Example:

```html
<label>Name</label>

<input type="text">
```

### Best Practice

Use the `for` attribute.

```html
<label for="name">Name</label>

<input type="text" id="name">
```

Clicking the label focuses the input.

---

# 5. `<input>`

The most commonly used form element.

Syntax:

```html
<input type="text">
```

---

# 6. Text Input

```html
<input type="text">
```

Example:

```html
<label>Name:</label>

<input type="text">
```

---

# 7. Placeholder

Displays hint text.

```html
<input
    type="text"
    placeholder="Enter your name">
```

---

# 8. Name Attribute

The `name` attribute is required if you want the field's value to be submitted.

```html
<input
    type="text"
    name="username">
```

---

# 9. Value Attribute

Sets the default value.

```html
<input
    type="text"
    value="John">
```

---

# 10. Required Field

```html
<input
    type="text"
    required>
```

The browser prevents submission until the field is filled.

---

# 11. Readonly

User cannot edit the value.

```html
<input
    type="text"
    value="India"
    readonly>
```

---

# 12. Disabled

Input cannot be used or submitted.

```html
<input
    type="text"
    disabled>
```

---

# 13. Size Attribute

Specifies the visible width of the input in characters.

```html
<input
    type="text"
    size="30">
```

---

# 14. Maxlength

Limits the number of characters.

```html
<input
    type="text"
    maxlength="10">
```

---

# 15. Input Types

## Text

```html
<input type="text">
```

Used for names and general text.

---

## Password

```html
<input type="password">
```

Characters are hidden.

---

## Email

```html
<input type="email">
```

Browser validates email format.

---

## Number

```html
<input
    type="number"
    min="1"
    max="100">
```

---

## Tel

```html
<input type="tel">
```

For phone numbers.

---

## URL

```html
<input type="url">
```

Validates website addresses.

---

## Search

```html
<input type="search">
```

Optimized for search fields.

---

## Date

```html
<input type="date">
```

---

## Time

```html
<input type="time">
```

---

## Datetime-local

```html
<input type="datetime-local">
```

---

## Month

```html
<input type="month">
```

---

## Week

```html
<input type="week">
```

---

## Color

```html
<input type="color">
```

Displays a color picker.

---

## Range

```html
<input
    type="range"
    min="0"
    max="100">
```

Creates a slider.

---

## Hidden

```html
<input
    type="hidden"
    value="123">
```

Stores hidden data.

---

# 16. Radio Buttons

Allows **only one** selection from a group.

```html
<input
    type="radio"
    name="gender"
    value="Male"> Male

<input
    type="radio"
    name="gender"
    value="Female"> Female
```

All radio buttons in the same group must share the **same `name`**.

---

# 17. Checkboxes

Allows multiple selections.

```html
<input
    type="checkbox"
    name="skill"
    value="HTML"> HTML

<input
    type="checkbox"
    name="skill"
    value="CSS"> CSS

<input
    type="checkbox"
    name="skill"
    value="JavaScript"> JavaScript
```

---

# 18. File Upload

```html
<input type="file">
```

Accept only images:

```html
<input
    type="file"
    accept="image/*">
```

Allow multiple files:

```html
<input
    type="file"
    multiple>
```

---

# 19. Submit Button

```html
<input
    type="submit"
    value="Register">
```

---

# 20. Reset Button

```html
<input
    type="reset">
```

Resets all fields to their initial values.

---

# 21. Button

```html
<button>Click Me</button>
```

Or

```html
<button type="submit">
    Submit
</button>
```

---

# 22. Textarea

For multi-line text.

```html
<textarea
    rows="5"
    cols="30">
</textarea>
```

---

# 23. Select (Drop-down)

```html
<select>

<option>India</option>

<option>USA</option>

<option>Canada</option>

</select>
```

---

## Selected Option

```html
<option selected>India</option>
```

---

## Grouping Options

```html
<select>

<optgroup label="Asia">

<option>India</option>

<option>Japan</option>

</optgroup>

<optgroup label="Europe">

<option>Germany</option>

<option>France</option>

</optgroup>

</select>
```

---

# 24. Datalist

Provides autocomplete suggestions while allowing custom input.

```html
<input
    list="cities">

<datalist id="cities">

<option value="Delhi">

<option value="Mumbai">

<option value="Bengaluru">

</datalist>
```

---

# 25. Fieldset and Legend

Groups related form controls.

```html
<fieldset>

<legend>Personal Information</legend>

<label>Name</label>

<input type="text">

</fieldset>
```

---

# 26. Browser Validation

Examples:

```html
<input
    type="email"
    required>
```

```html
<input
    type="number"
    min="18"
    max="60">
```

```html
<input
    type="text"
    pattern="[A-Za-z]{3,}">
```

---

# 27. Autocomplete

```html
<form autocomplete="on">
```

Disable:

```html
<form autocomplete="off">
```

---

# 28. Complete Registration Form

```html
<!DOCTYPE html>
<html>
<head>
    <title>Registration Form</title>
</head>
<body>

<h2>Student Registration</h2>

<form action="/submit" method="post">

<fieldset>

<legend>Personal Details</legend>

<label for="name">Name:</label><br>

<input
type="text"
id="name"
name="name"
placeholder="Enter your name"
required>

<br><br>

<label for="email">Email:</label><br>

<input
type="email"
id="email"
name="email"
required>

<br><br>

<label>Password:</label><br>

<input
type="password"
name="password"
required>

<br><br>

<label>Gender:</label><br>

<input
type="radio"
name="gender"
value="Male"> Male

<input
type="radio"
name="gender"
value="Female"> Female

<br><br>

<label>Skills:</label><br>

<input
type="checkbox"
name="skills"
value="HTML"> HTML

<input
type="checkbox"
name="skills"
value="CSS"> CSS

<input
type="checkbox"
name="skills"
value="JavaScript"> JavaScript

<br><br>

<label>Country:</label>

<select name="country">

<option>India</option>

<option>USA</option>

<option>Canada</option>

</select>

<br><br>

<label>About You</label><br>

<textarea
rows="5"
cols="30"></textarea>

<br><br>

<input
type="submit"
value="Register">

<input
type="reset">

</fieldset>

</form>

</body>
</html>
```

---

# Best Practices

* Always associate `<label>` with its corresponding input using `for` and `id`.
* Use meaningful `name` attributes for every field that should be submitted.
* Use `POST` for sensitive data such as passwords.
* Prefer HTML5 validation (`required`, `email`, `min`, `max`, `pattern`) before adding JavaScript.
* Group related controls with `<fieldset>` and `<legend>`.
* Use the most appropriate input type (`email`, `date`, `number`, etc.) to improve user experience.

---

# Summary Table

| Tag/Attribute   | Purpose                       |
| --------------- | ----------------------------- |
| `<form>`        | Creates a form                |
| `action`        | Submission URL                |
| `method`        | GET or POST                   |
| `<label>`       | Label for a form control      |
| `<input>`       | Input field                   |
| `type`          | Specifies input type          |
| `name`          | Name of submitted data        |
| `placeholder`   | Hint text                     |
| `value`         | Default value                 |
| `required`      | Makes a field mandatory       |
| `readonly`      | Prevents editing              |
| `disabled`      | Disables the field            |
| `<textarea>`    | Multi-line text input         |
| `<select>`      | Drop-down list                |
| `<option>`      | Item in a drop-down           |
| `<optgroup>`    | Group related options         |
| `<datalist>`    | Autocomplete suggestions      |
| `<fieldset>`    | Group related controls        |
| `<legend>`      | Title for a fieldset          |
| `pattern`       | Regular expression validation |
| `min` / `max`   | Numeric or date limits        |
| `<button>`      | Clickable button              |
| `type="submit"` | Submit the form               |
| `type="reset"`  | Reset the form                |

---
