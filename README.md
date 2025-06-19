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

- Behavior of Bootstrap classes changed to suit print media. No breakpoints, layout changed for fixed sizes
- Supports variables and directives like `@page`

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
    <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">Some quick example text.</p>
        <a href="#" class="btn btn-primary">Go somewhere</a>
    </div>
    <div class="card card-inlay">
        <div class="card-body center-middle text-center">
            <h5 class="card-title">Inlay Title</h5>
            <p class="card-text">This card has in inlay title.</p>
        </div>
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
