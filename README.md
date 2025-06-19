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

- Behavior changed to suit print media. No breakpoints, layout changed for fixed sizes
- Supports variables and directives like `@page`

### Bootstrap Features

- Typography styling
- Grid system
- Layout components
- Spacing utilities
- Color utilities
- Flexbox utilities

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

A demo document is available in the `demo` directory to showcase all the available components and utilities.

Since BootyPrint is a css framework for WeasyPrint, you need to use weasyprint in python to see the results. There is a npm script to install weasyprint and build the demo document.

```bash
$ npm run demo
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.
