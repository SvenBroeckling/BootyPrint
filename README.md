# BootyPrint

A lightweight Bootstrap alternative designed specifically for WeasyPrint.

## Installation

### Manual download

Download the CSS files from the releases section and include them in your project.

## Build from Source

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Build the CSS files:
   ```bash
   npm run build
   ```

This will generate both `bootyprint.css` and `bootyprint.min.css` in the `dist` folder.

## Usage

### Work in progress

The semantics of the BootyPrint classes, particularly those of the more complex components, are not yet stable and may
change with every version. While each change will be logged in the CHANGELOG, you should expect the classes to change.
However, the initial class structure will be largely stable by version 0.1.0.

### In HTML

```html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" href="path/to/bootyprint.css">
    <style>
        /* Custom variables for this template */
        :root {
            --primary: #3f51b5;
            --secondary: #2196f3;
            --font-size-base: 11px;
            --page-size: A4;
        }
    </style>
</head>
<body>
<!-- Your content here -->
</body>
</html>
```

## Features

The idea behind BootyStrap is to create a CSS library that behaves like Bootstrap but is designed for print media.
Consequently, BootyPrint lacks all the interactive features of Bootstrap, such as accordions and navbars, and there are
no breakpoints.

BootyStrap is designed for WeasyPrint and is tailored to its capabilities. If you use a different HTML-to-PDF rendering
engine, you may get different results.

### Grid System

BootyPrint includes a simplified 12-column grid system:

```html

<div class="container">
    <div class="row">
        <div class="col-6">Half width</div>
        <div class="col-6">Half width</div>
    </div>
</div>
```

### Flex Utilities

Flex utilities to create flex layouts:

```html

<div class="d-flex flex-column align-items-center">
    <div class="d-flex justify-content-between">
        <h2>I'm a h2!</h2>
        <h2>I'm a h2!</h2>
        <h2>I'm a h2!</h2>
    </div>
    <div class="d-flex justify-content-between">
        <h2>I'm a h2!</h2>
        <h2>I'm a h2!</h2>
        <h2>I'm a h2!</h2>
    </div>
</div>
```

### Typography

Basic typography classes are available:

```html
<h1 class="display-4">Large heading</h1>
<p class="lead">Lead paragraph</p>
<p class="text-muted">Muted text</p>
```

### Spacing

Margin and padding utilities:

```html

<div class="mt-3 mb-4 p-2">Spaced content</div>
```

### Sizing

Sizing utilities:

```html

<div class="w-100">Full width</div>
<div class="h-25">Quarter height</div>
```

### Colors

Background and text color utilities:

```html

<div class="bg-primary text-white">Colored box</div>
```

### Borders

Basic bootstrap border classes:

```html

<div class="border border-2 rounded">Rouned border</div>
<div class="border-start">Border left</div>
```

### Absolute Positioning

Utilities for setting absolute positioning values (top, bottom, left, right) and dimensions (width, height):

```html
<!-- Position elements with precise measurements -->
<div class="position-absolute top-10mm start-20mm width-50mm height-30mm">
    Absolutely positioned box
</div>

<!-- Available units: mm, cm, in -->
<div class="position-absolute bottom-2cm end-3cm width-5cm height-2cm">
    Positioned from bottom-right
</div>

<!-- Values from 0 to 600 are supported for each unit -->
<div class="position-absolute top-0mm start-0mm width-210mm height-297mm">
    Full A4 page overlay
</div>
```

### Columns

CSS Columns:

```html

<div class="columns-3">
    <p>
        Lorem ipsum dolor sit...
    </p>
</div>

<div class="columns-2 gap-5 rule-medium rule-primary text-justify text-hyphenate">
    <p>
        Lorem ipsum dolor sit...
    </p>
</div>

```

### Card Component

A card component:

```html

<div class="card">
    <h5 class="card-title">Card title</h5>
    <div class="card-body">
        <p class="card-text">Some quick example text.</p>
        <a href="#" class="btn btn-primary">Go somewhere</a>
    </div>

    <div class="card card-inlay">
        <h5 class="card-title">Inlay Title</h5>
        <div class="card-body center-middle text-center">
            <p class="card-text">This card has in inlay title.</p>
        </div>
    </div>
</div>

```

### Tables

BootyPrint includes various table styles:

```html
<!-- Basic Table -->
<table class="table">
    <thead>
    <tr>
        <th>ID</th>
        <th>Name</th>
        <th>Email</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>1</td>
        <td>John Doe</td>
        <td>john@example.com</td>
    </tr>
    <tr>
        <td>2</td>
        <td>Jane Smith</td>
        <td>jane@example.com</td>
    </tr>
    </tbody>
</table>

<!-- Striped Table -->
<table class="table table-striped">
    <caption>Striped Rows Table</caption>
    <!-- Table content... -->
</table>

<!-- Underlined Table -->
<table class="table table-underline">
    <caption>Table with Underlined Rows</caption>
    <!-- Table content... -->
</table>

<!-- Bordered Table -->
<table class="table table-bordered">
    <caption>Fully Bordered Table</caption>
    <!-- Table content... -->
</table>

<!-- Dotted Border Style -->
<table class="table table-bordered table-dotted">
    <caption>Table with Dotted Borders</caption>
    <!-- Table content... -->
</table>

<!-- Combining Styles -->
<table class="table table-striped table-underline table-compact">
    <caption>Compact Striped Table with Underlines</caption>
    <!-- Table content... -->
</table>
```

Table classes can be customized via CSS variables:

```css
:root {
    --table-cell-padding-y: 0.75rem;
    --table-border-color: #333;
    --table-striped-bg: rgba(0, 123, 255, 0.1);
}
```

### Chapters

Chapters are intended for use in book printing. They behave as follows:

- The chapter always starts on the right-hand page.
- A page break is always made before the chapter; it never starts on a half page.
- Images are full width by default.

In order to use a chapter, the pages should be set up with alternating page margins to accommodate the inner gutter of the printed book.

```css
@page :left {
    margin: 20mm 30mm 20mm 20mm;
    @bottom-left {
        content: counter(page);
    }
}

@page :right {
    margin: 20mm 20mm 20mm 30mm;
    @bottom-right {
        content: counter(page);
    }
}
```

```html
<div class="chapter">
    <!-- Content -->
</div>

<div class="chapter">
    <div class="columns-2 gap-4">
        <!-- Content with columns -->
    </div>
</div>
```

## Demo

A [demo document](demo/demo.pdf) is available in the `demo` directory to showcase all the available components and
utilities.

Since BootyPrint is a css framework for WeasyPrint, you need to use weasyprint in python to see the results. There is a
npm script to install weasyprint and build the demo document.

```bash
$ npm run demo
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.
