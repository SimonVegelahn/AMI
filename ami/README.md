# AMI Design System

An accessible, friendly, and welcoming CSS design system.

I wanted to create an accessible, friendly and welcoming design theme for my projects. AMI prioritizes readability, WCAG AA/AAA compliance, and a warm visual aesthetic that doesn't sacrifice professionalism.

![AMI Preview](preview.png)

---

## Features

- **Accessibility First** — WCAG AA baseline, AAA for interactive elements
- **Light & Welcoming** — Warm whites, friendly rounded corners (4-6px)
- **Dual Typography** — Sans-serif headings (Inter), serif body text (Source Serif 4)
- **Eye-Gentle Theme** — Reduced contrast mode for extended reading
- **Zero JavaScript** — Pure CSS, works everywhere
- **~15KB minified** — Lightweight, no bloat

---

## Quick Start

### Option 1: CDN (Recommended for prototyping)

Add directly to your HTML:

```html
<link rel="stylesheet" href="https://unpkg.com/ami-css@3/ami.min.css">
```

Or use jsDelivr:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/ami-css@3/ami.min.css">
```

### Option 2: npm

```bash
npm install ami-css
```

Then import in your CSS or bundler:

```css
@import 'ami-css';
```

### Option 3: Download

Download the files and include in your project:

```html
<link rel="stylesheet" href="path/to/ami.css">
```

Or for production:

```html
<link rel="stylesheet" href="path/to/ami.min.css">
```

---

## File Structure

| File | Purpose | Size |
|------|---------|------|
| `ami.css` | Main entry point (imports all) | — |
| `ami.min.css` | Production build | ~15KB |
| `01-tokens.css` | Design tokens & CSS variables | 18KB |
| `02-reset.css` | Reset & base typography | 11KB |
| `03-components.css` | Buttons, forms, cards, etc. | 18KB |
| `04-data-display.css` | Tables, tabs, modals, nav | 15KB |
| `05-utilities.css` | Layout & utility classes | 20KB |

---

## Usage

### Basic HTML Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Project</title>
  <link rel="stylesheet" href="https://unpkg.com/ami-css@3/ami.min.css">
</head>
<body>
  <main class="container py-12">
    <h1>Welcome</h1>
    <p>Your content here.</p>
  </main>
</body>
</html>
```

### Themes

AMI ships with two themes:

```html
<!-- Default light theme -->
<html data-theme="light">

<!-- Eye-gentle theme (reduced contrast, warmer tones) -->
<html data-theme="gentle">
```

---

## Components

### Buttons

```html
<button class="btn btn-primary">Primary</button>
<button class="btn btn-secondary">Secondary</button>
<button class="btn btn-ghost">Ghost</button>
<button class="btn btn-danger">Danger</button>

<!-- Sizes -->
<button class="btn btn-primary btn-sm">Small</button>
<button class="btn btn-primary btn-lg">Large</button>
```

### Form Inputs

```html
<div class="form-group">
  <label class="form-label">Email</label>
  <input type="email" class="input" placeholder="you@example.com">
  <span class="form-helper">We'll never share your email.</span>
</div>

<!-- With validation -->
<input type="text" class="input input-error">
<span class="form-error">This field is required.</span>
```

### Cards

```html
<div class="card">
  <div class="card-header">
    <h3 class="card-title">Card Title</h3>
    <p class="card-description">Optional description text.</p>
  </div>
  <div class="card-body">
    Card content goes here.
  </div>
  <div class="card-footer">
    <button class="btn btn-primary">Action</button>
  </div>
</div>
```

### Alerts

```html
<div class="alert alert-info">
  <div class="alert-content">
    <div class="alert-title">Information</div>
    <div class="alert-description">This is an informational message.</div>
  </div>
</div>

<!-- Variants: alert-success, alert-warning, alert-error -->
```

### Badges

```html
<span class="badge badge-default">Default</span>
<span class="badge badge-primary">Primary</span>
<span class="badge badge-success">Success</span>
<span class="badge badge-warning">Warning</span>
<span class="badge badge-error">Error</span>
```

### Tables

```html
<table class="table table-striped table-hover">
  <thead>
    <tr>
      <th>Name</th>
      <th>Status</th>
      <th class="cell-numeric">Amount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Item One</td>
      <td><span class="badge badge-success">Active</span></td>
      <td class="cell-numeric">$1,234</td>
    </tr>
  </tbody>
</table>
```

### Navigation

```html
<nav class="nav">
  <a href="/" class="nav-brand">Brand</a>
  <div class="nav-menu">
    <a href="#" class="nav-link active">Home</a>
    <a href="#" class="nav-link">Features</a>
    <a href="#" class="nav-link">Pricing</a>
  </div>
  <div class="nav-actions">
    <button class="btn btn-primary btn-sm">Sign Up</button>
  </div>
</nav>
```

### Tabs

```html
<div class="tabs">
  <div class="tabs-list">
    <button class="tabs-trigger active">Tab 1</button>
    <button class="tabs-trigger">Tab 2</button>
    <button class="tabs-trigger">Tab 3</button>
  </div>
  <div class="tabs-content">
    <div class="tabs-panel active">Content for tab 1</div>
    <div class="tabs-panel">Content for tab 2</div>
    <div class="tabs-panel">Content for tab 3</div>
  </div>
</div>
```

---

## Utilities

### Layout

```html
<div class="container">Centered container</div>
<div class="flex justify-between items-center">Flexbox</div>
<div class="grid grid-cols-3 gap-4">Grid</div>
```

### Spacing

```html
<div class="p-4">Padding 16px</div>
<div class="mt-8 mb-4">Margin top 32px, bottom 16px</div>
<div class="px-6 py-4">Padding x 24px, y 16px</div>
```

### Typography

```html
<p class="text-lg font-semibold">Large semibold text</p>
<p class="text-muted text-sm">Small muted text</p>
<p class="font-serif">Serif font family</p>
```

---

## Customization

Override CSS variables to customize the theme:

```css
:root {
  --primary: #2563eb;           /* Change primary color */
  --primary-hover: #1d4ed8;
  --font-sans: 'Your Font', sans-serif;
  --radius-md: 8px;             /* Rounder corners */
}
```

---

## Browser Support

- Chrome 88+
- Firefox 78+
- Safari 14+
- Edge 88+

---

## Contributing

Contributions are welcome! Please open an issue first to discuss proposed changes.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## License

MIT License — see [LICENSE](LICENSE) for details.

Attribution appreciated but not required for use.

---

## Credits

- Typography: [Inter](https://rsms.me/inter/), [Source Serif 4](https://github.com/adobe-fonts/source-serif), [JetBrains Mono](https://www.jetbrains.com/lp/mono/)
- Inspiration: Tailwind CSS, Radix UI, shadcn/ui
