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
## 4. Essential Properties

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
## 5. Animations

```css
/* First, define our keyframes for different animations */
@keyframes slideIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes pulse {
    0% {
        transform: scale(1);
    }
    50% {
        transform: scale(1.02);
    }
    100% {
        transform: scale(1);
    }
}

@keyframes shake {
    0%, 100% {
        transform: translateX(0);
    }
    25% {
        transform: translateX(-5px);
    }
    75% {
        transform: translateX(5px);
    }
}

/* Add entrance animation to the form */
main {
    /* Keep existing styles... */
    animation: slideIn 0.6s ease-out;
}

/* Stagger the entrance of form elements */
.form-group {
    /* Keep existing styles... */
    animation: slideIn 0.6s ease-out;
    animation-fill-mode: both;
}

/* Stagger each form group's entrance */
.form-group:nth-child(1) { animation-delay: 0.1s; }
.form-group:nth-child(2) { animation-delay: 0.2s; }
.form-group:nth-child(3) { animation-delay: 0.3s; }
.form-group:nth-child(4) { animation-delay: 0.4s; }
.form-group:nth-child(5) { animation-delay: 0.5s; }

/* Add hover animation to inputs */
input[type="text"]:hover,
input[type="email"]:hover,
textarea:hover,
select:hover {
    /* Keep existing styles... */
    animation: pulse 0.5s ease-in-out;
}

/* Enhanced focus animations */
input[type="text"]:focus,
input[type="email"]:focus,
textarea:focus,
select:focus {
    /* Keep existing styles... */
    animation: pulse 0.3s ease-in-out;
}

/* Submit button animations */
button[type="submit"] {
    /* Keep existing styles... */
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
}

button[type="submit"]:hover {
    /* Keep existing styles... */
    transform: translateY(-2px);
    box-shadow: 0 4px 12px rgba(0, 102, 204, 0.2);
}

button[type="submit"]:active {
    transform: translateY(0);
}

/* Add ripple effect on button */
button[type="submit"]::after {
    content: '';
    position: absolute;
    top: 50%;
    left: 50%;
    width: 0;
    height: 0;
    background: rgba(255, 255, 255, 0.2);
    border-radius: 50%;
    transform: translate(-50%, -50%);
    transition: width 0.3s, height 0.3s;
}

button[type="submit"]:active::after {
    width: 200px;
    height: 200px;
}

/* Add error state animation */
.form-group.error input,
.form-group.error textarea,
.form-group.error select {
    border-color: #ff3b30;
    animation: shake 0.4s ease-in-out;
}

/* Success feedback animation */
.form-group.success input,
.form-group.success textarea,
.form-group.success select {
    border-color: #34c759;
    animation: pulse 0.4s ease-in-out;
}
