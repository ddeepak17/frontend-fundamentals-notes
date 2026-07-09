# HTML/CSS Basics

## 1. HTML Structure and Semantic Tags

HTML is used to structure the content on a webpage. It tells the browser what each part of the page is, like headings, paragraphs, links, forms, images, and sections.

A basic HTML page looks like this:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Page</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

The `head` section is mostly for information about the page, like the title, metadata, and links to CSS files. The `body` section contains the actual content that users see on the webpage.

## Semantic Tags

Semantic tags are tags that clearly describe what the content is meant for. Instead of using only `div` tags everywhere, semantic tags make the page easier to read and understand.

Examples:

- `<header>`: top section of a page or section
- `<nav>`: navigation links
- `<main>`: main page content
- `<section>`: a section of related content
- `<article>`: independent content, like a post or card
- `<aside>`: side content
- `<footer>`: bottom section of the page

Example:

```html
<header>
  <h1>My Website</h1>
</header>

<nav>
  <a href="/">Home</a>
  <a href="/about">About</a>
</nav>

<main>
  <section>
    <h2>About</h2>
    <p>This section contains information about the website.</p>
  </section>
</main>

<footer>
  <p>Copyright 2026</p>
</footer>
```

My understanding: semantic tags make the structure of a page clearer. For example, if I see `<nav>`, I know that part is for navigation. If I see `<main>`, I know that is the main content area.

---

## 2. Forms, Tables, Lists, and Inputs

### Forms

Forms are used to collect input from users. Common examples are login forms, contact forms, search bars, and signup forms.

Example:

```html
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" />

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" />

  <button type="submit">Submit</button>
</form>
```

Common form elements:

- `<form>`: creates the form
- `<label>`: describes the input
- `<input>`: collects user input
- `<textarea>`: for longer text
- `<select>`: dropdown menu
- `<button>`: clickable button

Common input types:

- `text`
- `email`
- `password`
- `number`
- `checkbox`
- `radio`
- `date`
- `file`
- `submit`

My understanding: labels are important because they make the form easier to use and more accessible. The `for` in the label should match the `id` of the input.

---

### Lists

Lists are used to group related items.

Unordered list:

```html
<ul>
  <li>React</li>
  <li>JavaScript</li>
  <li>CSS</li>
</ul>
```

Ordered list:

```html
<ol>
  <li>Install dependencies</li>
  <li>Run the app</li>
  <li>Test the app</li>
</ol>
```

My understanding: unordered lists are for items where order does not matter, and ordered lists are for steps where order matters.

---

### Tables

Tables are used to show structured data in rows and columns.

Example:

```html
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Role</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Darren</td>
      <td>Intern</td>
    </tr>
  </tbody>
</table>
```

Common table tags:

- `<table>`: creates the table
- `<thead>`: header section
- `<tbody>`: main body section
- `<tr>`: table row
- `<th>`: table heading cell
- `<td>`: table data cell

My understanding: tables should be used for actual structured data, not just for page layout.

---

## 3. CSS Selectors and Styling

CSS is used to style HTML elements. It controls things like colors, spacing, fonts, borders, and layout.

Basic syntax:

```css
selector {
  property: value;
}
```

Example:

```css
p {
  color: blue;
  font-size: 16px;
}
```

### Common CSS Selectors

Element selector:

```css
h1 {
  color: black;
}
```

This applies to all `h1` elements.

Class selector:

```css
.card {
  padding: 20px;
  border: 1px solid #ccc;
}
```

This applies to any element with `class="card"`.

ID selector:

```css
#main-title {
  font-size: 32px;
}
```

This applies to the element with `id="main-title"`.

Descendant selector:

```css
nav a {
  text-decoration: none;
}
```

This applies to all links inside a `nav`.

### Common CSS Properties

Some common CSS properties are:

- `color`
- `background-color`
- `font-size`
- `font-family`
- `margin`
- `padding`
- `border`
- `border-radius`
- `display`
- `width`
- `height`

Example:

```css
.card {
  background-color: white;
  padding: 16px;
  border-radius: 8px;
  margin-bottom: 12px;
}
```

### Margin vs Padding

- `margin` is space outside an element.
- `padding` is space inside an element.

Example:

```css
.box {
  margin: 20px;
  padding: 16px;
}
```

My understanding: CSS selectors decide what element gets styled, and CSS properties decide how it looks.

---

## 4. Flexbox and Grid

Flexbox and Grid are used for layouts in CSS.

### Flexbox

Flexbox is useful when arranging items in one direction, either row or column.

Example:

```css
.container {
  display: flex;
  gap: 16px;
  justify-content: center;
  align-items: center;
}
```

Common Flexbox properties:

- `display: flex`
- `flex-direction`
- `justify-content`
- `align-items`
- `gap`
- `flex-wrap`

Example:

```html
<div class="container">
  <div>Box 1</div>
  <div>Box 2</div>
  <div>Box 3</div>
</div>
```

```css
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

Flexbox is useful for:

- navbars
- buttons in a row
- cards in a row
- centering content
- simple horizontal or vertical layouts

My understanding: Flexbox is usually the best choice when I need to align items in one direction.

---

### Grid

CSS Grid is useful for layouts with rows and columns.

Example:

```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}
```

Example HTML:

```html
<div class="grid">
  <div>Card 1</div>
  <div>Card 2</div>
  <div>Card 3</div>
</div>
```

Common Grid properties:

- `display: grid`
- `grid-template-columns`
- `grid-template-rows`
- `gap`
- `grid-column`
- `grid-row`

Grid is useful for:

- dashboards
- image galleries
- card layouts
- full page layouts

My understanding: Flexbox is better for one-direction layouts, while Grid is better when I need both rows and columns.

---

## 5. Responsive Design Basics

Responsive design means making a website work properly on different screen sizes like phones, tablets, laptops, and desktops.

Important ideas:

- Use flexible widths.
- Avoid fixed layouts when possible.
- Use media queries.
- Use relative units like `%`, `rem`, `em`, `vw`, and `vh`.
- Make images responsive.
- Test the layout on smaller screens.

Responsive image example:

```css
img {
  max-width: 100%;
  height: auto;
}
```

This makes sure the image does not overflow outside its container.

### Media Queries

Media queries let CSS change depending on screen size.

Example:

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

@media (max-width: 768px) {
  .container {
    grid-template-columns: 1fr;
  }
}
```

This means the layout has 3 columns on larger screens, but switches to 1 column on smaller screens.

Common breakpoints:

- `480px` for small phones
- `768px` for tablets
- `1024px` for laptops
- `1200px` and above for larger screens

My understanding: responsive design is important because users may open the same website on different devices. The layout should still be readable and easy to use.

---

## Quick Summary

HTML is used for structure. CSS is used for styling and layout. Semantic tags make HTML easier to understand. Forms collect user input, lists group items, and tables show structured data. Flexbox is useful for one-direction layouts, while Grid is better for rows and columns. Responsive design makes the page work well on different screen sizes.
