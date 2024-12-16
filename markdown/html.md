# HTML Fundamentals

## 1. Introduction to HTML

HTML (HyperText Markup Language) is the standard markup language used to create the structure and content of web pages. It uses elements and tags to define different parts of a webpage, like headings, paragraphs, images, and links.

### Document Structure

Every HTML document follows a standard structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Webpage</title>
</head>
<body>
    <!-- Content goes here -->
</body>
</html>
```

Breaking down each part:

- `<!DOCTYPE html>`: Declares that this is an HTML5 document
- `<html>`: The root element containing all other elements
- `<head>`: Contains metadata about the document
- `<meta>`: Provides additional information about the webpage
- `<title>`: Sets the page title shown in the browser tab
- `<body>`: Contains the visible content of the webpage

---
## 2. Essential HTML Elements

### Headings

HTML provides six levels of headings:

```html
<h1>Main Heading</h1>
<h2>Subheading</h2>
<h3>Sub-subheading</h3>
<!-- h4, h5, and h6 follow the same pattern -->
 ```

### Paragraphs and Text

```html
<p>This is a paragraph of text.</p>
<strong>Bold text</strong>
<em>Italic text</em>
<br> <!-- Line break -->
```

### Lists

```html
<!-- Unordered list -->
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
</ul>

<!-- Ordered list -->
<ol>
    <li>First item</li>
    <li>Second item</li>
</ol>
```

### Links

```html
<a href="https://example.com">Click here to visit Example.com</a>
```

### Images

```html
<img src="path/to/image.jpg" alt="Description of the image">
```
---

## 3. Best practices

1. Always use semantic HTML elements that describe their content's purpose
2. Include proper indentation for better code readability
3. Use descriptive alt text for images
4. Ensure proper nesting of elements
5. Use lowercase for element names and attributes

### Common semantic examples

```html
<header>: Header content
<nav>: Navigation links
<main>: Main content
<article>: Independent content
<section>: Grouped content
<footer>: Footer content
```
---

## 4. Advanced HTML

### Forms and User Input

Forms are essential for collecting user input on websites. They enable everything from search functionality to user registration.

**Basic Form Structure**

```html
<form action="/submit" method="POST">
    <!-- Form elements go here -->
</form>
```

The `action` attribute specifies where the form data should be sent, while `method` determines how it's sent (`GET` or `POST`).

**Common Input Types**

```html
<!-- Text input with label -->
<label for="username">Username:</label>
<input type="text" id="username" name="username" placeholder="Enter your username">

<!-- Password field -->
<input type="password" name="password" placeholder="Enter your password">

<!-- Email field with validation -->
<input type="email" name="email" required>

<!-- Number input with constraints -->
<input type="number" name="age" min="0" max="120">

<!-- Date picker -->
<input type="date" name="birthdate">

<!-- File upload -->
<input type="file" name="document" accept=".pdf,.doc,.docx">

<!-- Radio buttons -->
<fieldset>
    <legend>Select your plan:</legend>
    <input type="radio" id="basic" name="plan" value="basic">
    <label for="basic">Basic</label>
    <input type="radio" id="premium" name="plan" value="premium">
    <label for="premium">Premium</label>
</fieldset>

<!-- Checkboxes -->
<input type="checkbox" id="terms" name="terms" required>
<label for="terms">I agree to the terms</label>

<!-- Dropdown select -->
<select name="country">
    <option value="">Select a country</option>
    <option value="us">United States</option>
    <option value="uk">United Kingdom</option>
</select>

<!-- Text area -->
<textarea name="message" rows="4" cols="50">
Enter your message here...
</textarea>

<!-- Submit button -->
<button type="submit">Submit Form</button>
```

---
### Tables

Tables are used to display structured data in rows and columns.

```html
<table>
    <caption>Monthly Sales Data</caption>
    <thead>
        <tr>
            <th scope="col">Month</th>
            <th scope="col">Sales</th>
            <th scope="col">Growth</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>January</td>
            <td>$10,000</td>
            <td>10%</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="3">Annual Total: $120,000</td>
        </tr>
    </tfoot>
</table>
```

---
### Advanced Semantic Elements

**Article vs Section**

```html
<article>
    <!-- Used for self-contained content that makes sense on its own -->
    <h2>Blog Post Title</h2>
    <p>Blog content...</p>
</article>

<section>
    <!-- Used for grouping related content -->
    <h2>Featured Products</h2>
    <!-- Product listings -->
</section>
```

---

### Metadata and SEO

```html
<head>
    <!-- Character encoding -->
    <meta charset="UTF-8">
    
    <!-- Viewport settings for responsive design -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- SEO meta tags -->
    <meta name="description" content="Page description for search engines">
    <meta name="keywords" content="html, web development, tutorial">
    
    <!-- Social media meta tags -->
    <meta property="og:title" content="Page Title">
    <meta property="og:description" content="Page description">
    <meta property="og:image" content="image.jpg">
    
    <!-- Favicon -->
    <link rel="icon" type="image/x-icon" href="favicon.ico">
</head>
```

