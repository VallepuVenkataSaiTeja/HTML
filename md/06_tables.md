# HTML Tables

HTML tables are used to display data in **rows and columns**. They are ideal for structured information such as marksheets, employee details, product lists, schedules, and reports.

> **Note:** Tables should be used for **tabular data**, not for creating page layouts.

---

# 1. Basic Table Structure

A table consists of:

* `<table>` → Creates the table
* `<tr>` → Table Row
* `<th>` → Table Header
* `<td>` → Table Data (Cell)

## Syntax

```html
<table>
    <tr>
        <th>Header</th>
        <th>Header</th>
    </tr>

    <tr>
        <td>Data</td>
        <td>Data</td>
    </tr>
</table>
```

---

# 2. Simple Table

```html
<table>
    <tr>
        <th>Name</th>
        <th>Age</th>
        <th>City</th>
    </tr>

    <tr>
        <td>John</td>
        <td>22</td>
        <td>Delhi</td>
    </tr>

    <tr>
        <td>Alice</td>
        <td>20</td>
        <td>Mumbai</td>
    </tr>
</table>
```

### Output

| Name  | Age | City   |
| ----- | --: | ------ |
| John  |  22 | Delhi  |
| Alice |  20 | Mumbai |

---

# 3. Border Attribute

Older HTML used the `border` attribute.

```html
<table border="1">
    <tr>
        <td>HTML</td>
        <td>CSS</td>
    </tr>
</table>
```

> **Note:** The `border` attribute is obsolete in HTML5. Use CSS instead.

---

# 4. Table Border Using CSS

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

```css
table, th, td {
    border: 1px solid black;
}

table {
    border-collapse: collapse;
}
```

---

# 5. `border-collapse`

Removes the double border between cells.

Without:

```text
+----++----+
| A  || B  |
+----++----+
```

With:

```css
table {
    border-collapse: collapse;
}
```

Output:

```text
+---------+
| A | B   |
+---------+
```

---

# 6. Cell Padding

Adds space inside table cells.

```css
th, td {
    padding: 10px;
}
```

---

# 7. Cell Spacing

Older HTML:

```html
<table cellspacing="10">
```

Modern CSS:

```css
table {
    border-spacing: 10px;
}
```

---

# 8. Table Width

```css
table {
    width: 100%;
}
```

Or

```css
table {
    width: 500px;
}
```

---

# 9. Table Caption

Adds a title to the table.

```html
<table>
    <caption>Student Details</caption>

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

---

# 10. Column Span (`colspan`)

Allows one cell to span multiple columns.

```html
<table border="1">
    <tr>
        <th colspan="2">Student Information</th>
    </tr>

    <tr>
        <td>Name</td>
        <td>John</td>
    </tr>
</table>
```

Output:

| Student Information |      |
| ------------------- | ---- |
| Name                | John |

---

# 11. Row Span (`rowspan`)

Allows one cell to span multiple rows.

```html
<table border="1">
    <tr>
        <th rowspan="2">Name</th>
        <td>John</td>
    </tr>

    <tr>
        <td>Alice</td>
    </tr>
</table>
```

Output:

| Name | John  |
| ---- | ----- |
|      | Alice |

---

# 12. Combining `rowspan` and `colspan`

```html
<table border="1">
    <tr>
        <th rowspan="2">Name</th>
        <th colspan="2">Marks</th>
    </tr>

    <tr>
        <th>Math</th>
        <th>Science</th>
    </tr>

    <tr>
        <td>John</td>
        <td>90</td>
        <td>85</td>
    </tr>
</table>
```

---

# 13. Table Sections

HTML provides semantic sections.

* `<thead>` → Header
* `<tbody>` → Main data
* `<tfoot>` → Footer

Example:

```html
<table>

    <thead>
        <tr>
            <th>Name</th>
            <th>Marks</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>John</td>
            <td>95</td>
        </tr>

        <tr>
            <td>Alice</td>
            <td>88</td>
        </tr>
    </tbody>

    <tfoot>
        <tr>
            <td>Total Students</td>
            <td>2</td>
        </tr>
    </tfoot>

</table>
```

---

# 14. Styling Tables

```css
table {
    width: 100%;
    border-collapse: collapse;
}

th {
    background-color: lightgray;
}

th, td {
    border: 1px solid black;
    padding: 10px;
    text-align: center;
}
```

---

# 15. Alternating Row Colors

```css
tr:nth-child(even) {
    background-color: #f2f2f2;
}
```

This improves readability.

---

# 16. Hover Effect

```css
tr:hover {
    background-color: lightyellow;
}
```

---

# 17. Responsive Tables

For wide tables, wrap them in a container.

```html
<div class="table-container">
    <table>
        ...
    </table>
</div>
```

```css
.table-container {
    overflow-x: auto;
}
```

This allows horizontal scrolling on smaller screens.

---

# 18. Common Use Cases

Tables are useful for:

* Student marks
* Employee records
* Product lists
* Timetables
* Pricing tables
* Reports

Example:

```html
<table>
    <tr>
        <th>Product</th>
        <th>Price</th>
    </tr>

    <tr>
        <td>Laptop</td>
        <td>$900</td>
    </tr>
</table>
```

---

# 19. Complete Example

```html
<!DOCTYPE html>
<html>
<head>

<style>

table {
    width: 100%;
    border-collapse: collapse;
}

th, td {
    border: 1px solid black;
    padding: 10px;
    text-align: center;
}

th {
    background-color: lightgray;
}

tr:nth-child(even) {
    background-color: #f2f2f2;
}

tr:hover {
    background-color: lightyellow;
}

caption {
    font-size: 22px;
    font-weight: bold;
    margin-bottom: 10px;
}

</style>

</head>

<body>

<table>

<caption>Student Report</caption>

<thead>
<tr>
<th>Name</th>
<th>Age</th>
<th>Marks</th>
</tr>
</thead>

<tbody>

<tr>
<td>John</td>
<td>22</td>
<td>90</td>
</tr>

<tr>
<td>Alice</td>
<td>20</td>
<td>95</td>
</tr>

<tr>
<td>David</td>
<td>21</td>
<td>88</td>
</tr>

</tbody>

<tfoot>

<tr>
<td colspan="2">Average Marks</td>
<td>91</td>
</tr>

</tfoot>

</table>

</body>
</html>
```

---

# Best Practices

* ✅ Use `<th>` for header cells.
* ✅ Use `<caption>` to describe the table.
* ✅ Use `<thead>`, `<tbody>`, and `<tfoot>` for better structure.
* ✅ Use CSS for styling instead of obsolete HTML attributes.
* ✅ Use `border-collapse: collapse;` for clean borders.
* ✅ Use tables only for tabular data, not page layouts.
* ✅ Make wide tables responsive with `overflow-x: auto`.

---

# Summary Table

| Tag/Attribute      | Purpose                                 |
| ------------------ | --------------------------------------- |
| `<table>`          | Creates a table                         |
| `<tr>`             | Table row                               |
| `<th>`             | Header cell                             |
| `<td>`             | Data cell                               |
| `<caption>`        | Table title                             |
| `<thead>`          | Header section                          |
| `<tbody>`          | Main table content                      |
| `<tfoot>`          | Footer section                          |
| `colspan`          | Span a cell across multiple columns     |
| `rowspan`          | Span a cell across multiple rows        |
| `border-collapse`  | Merge adjacent borders                  |
| `padding`          | Space inside cells                      |
| `border-spacing`   | Space between cells                     |
| `text-align`       | Align text in cells                     |
| `overflow-x: auto` | Make tables scrollable on small screens |

---