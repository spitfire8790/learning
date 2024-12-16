# CSS Fundamentals

## 1. Introduction to CSS

CSS (Cascading Style Sheets) is a styling language that controls the visual presentation of HTML elements. The term "cascading" refers to how styles can inherit and override each other based on specificity rules. Think of HTML as the skeleton of a webpage, while CSS is the skin and clothing that makes it visually appealing.

## 2. Ways to include CSS 

### Inline CSS

Inline CSS is written directly in the HTML element using the style attribute:

```html
<p style="color: blue; font-size: 16px;">This is blue text</p>
```

While immediate, inline CSS isn't recommended for larger projects as it mixes content with presentation and makes maintenance difficult.

### Internal CSS

Internal CSS is placed within a `<style>` tag in the HTML document's head:

```html
<head>
    <style>
        p {
            color: blue;
            font-size: 16px;
        }
    </style>
</head>
```

This method is useful for single-page websites but becomes inefficient for multiple pages.

### External CSS (Recommended)

External CSS lives in a separate .css file and is linked to the HTML:

```html
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```

This is the preferred method as it promotes reusability and easier maintenance.

## 3. CSS Syntax and Selectors

### Basic Syntax

```css
selector {
    property: value;
    another-property: value;
}
```
### Common Selectors

**Element Selector**

Targets all instances of an HTML element:

```css
p {
    color: navy;
}
```

**Class Selector**

Targets elements with a specific class:

```css
.highlight {
    background-color: yellow;
}
```

**ID Selector**

Targets a unique element with a specific ID:

```css
#header {
    background-color: black;
    color: white;
}
```

**Descendant Selector**

Targets elements nested within other elements:

```css
article p {
    line-height: 1.6;
}
```

**Multiple Selectors**

Apply the same styles to multiple selectors:

```css
h1, h2, h3 {
    font-family: Arial, sans-serif;
}
```

---
## 3. Essential Properties

### Text Styling

```css
p {
    color: #333333;                 /* Text color */
    font-family: Arial, sans-serif; /* Font with fallback */
    font-size: 16px;                /* Text size */
    font-weight: bold;              /* Text weight */
    text-align: center;             /* Text alignment */
    line-height: 1.5;               /* Line spacing */
    text-decoration: underline;     /* Text decoration */
}
```

### Box Model

Every HTML element is a box with these properties:

```css
div {
    margin: 10px;            /* Space outside the border */
    border: 1px solid black; /* Border around the element */
    padding: 15px;           /* Space between content and border */
    width: 300px;            /* Element width */
    height: 200px;           /* Element height */
}
```

### Colors and Backgrounds

```css
div {
    background-color: #f0f0f0;         /* Solid background color */
    background-image: url('bg.jpg');   /* Background image */
    background-size: cover;            /* Image sizing */
    background-position: center;       /* Image position */
    opacity: 0.9;                      /* Element transparency */
}
```

### Units of Measurement

CSS supports various units:

```css
div {
    /* Absolute units */
    width: 100px;    /* Pixels */
    margin: 1in;     /* Inches */
    padding: 1cm;    /* Centimeters */

    /* Relative units */
    font-size: 2em;    /* Relative to parent element */
    width: 50%;        /* Percentage of parent */
    height: 100vh;     /* Viewport height */
    padding: 1rem;     /* Relative to root element */
}
```

