# BootyPrint

A lightweight Bootstrap alternative designed specifically for WeasyPrint. This library provides a simplified version of
Bootstrap's core functionality that works well with WeasyPrint for PDF generation.

## Features

- Behavior changed to suit print media. No breakpoint, layout changed for fixed sizes
- Supports variables and directives like `@page`
- Modern build system with SCSS source files
- Minified and full versions available

### Bootstrap Features

- Typography styling
- Grid system
- Layout components
- Spacing utilities
- Color utilities
- Flexbox utilities

### Components

While most bootstrap components are not supported, BootyPrint brings some own components.

- Box

## Installation

### Using npm

```bash
npm install bootyprint
```

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
    <style>
        /* Custom variables for this template */
        :root {
            --primary: #3f51b5;
            --secondary: #2196f3;
            --font-size-base: 12px;
        }
    </style>
   <link rel="stylesheet" href="path/to/bootyprint.css">
</head>
<body>
    <!-- Your content here -->
</body>
</html>
```

## Components

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

### Colors

Background and text color utilities:

```html
<div class="bg-primary text-white">Colored box</div>
```

## Demo

A demo page is available in the `demo` directory to showcase all the available components and utilities.

Since BootyPrint is a css framework for WeasyPrint, you need to use weasyprint in python to see the results.

```bash
$ python -m venv .venv
$ . .venv/bin/activate
$ pip install weasyprint
$ weasyprint demo/demo.html demo/demo.pdf
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.
