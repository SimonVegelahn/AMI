# AMI Usage Documentation

Complete reference for all AMI components and utilities.

---

## Table of Contents

1. [Installation](#installation)
2. [Themes](#themes)
3. [Typography](#typography)
4. [Buttons](#buttons)
5. [Form Elements](#form-elements)
6. [Cards](#cards)
7. [Alerts](#alerts)
8. [Badges](#badges)
9. [Avatars](#avatars)
10. [Tables](#tables)
11. [Tabs](#tabs)
12. [Navigation](#navigation)
13. [Modal](#modal)
14. [Accordion](#accordion)
15. [Lists](#lists)
16. [Pagination](#pagination)
17. [Loading States](#loading-states)
18. [Utilities](#utilities)
19. [Customization](#customization)

---

## Installation

### CDN

```html
<!-- Development -->
<link rel="stylesheet" href="https://unpkg.com/ami-css@3/ami.css">

<!-- Production (minified) -->
<link rel="stylesheet" href="https://unpkg.com/ami-css@3/ami.min.css">
```

### npm

```bash
npm install ami-css
```

```css
/* In your CSS */
@import 'ami-css';

/* Or in JavaScript/bundler */
import 'ami-css';
```

### Direct Download

Download from GitHub and include:

```html
<link rel="stylesheet" href="path/to/ami.min.css">
```

---

## Themes

AMI includes two themes: Light (default) and Eye-Gentle.

```html
<!-- Light theme (default) -->
<html data-theme="light">

<!-- Eye-gentle theme (reduced contrast, warmer tones) -->
<html data-theme="gentle">
```

### Dark Sections

Use `.section-dark` for dark regions within a light page:

```html
<section class="section-dark p-8">
  <h2>Dark Section</h2>
  <p>This section has dark background with light text.</p>
</section>
```

---

## Typography

### Headings

```html
<h1>Heading 1 (36px)</h1>
<h2>Heading 2 (30px)</h2>
<h3>Heading 3 (24px)</h3>
<h4>Heading 4 (20px)</h4>
<h5>Heading 5 (18px)</h5>
<h6>Heading 6 (16px)</h6>
```

### Body Text

```html
<p>Default paragraph text uses Source Serif 4.</p>
<p class="text-secondary">Secondary text with reduced emphasis.</p>
<p class="text-muted">Muted text for supplementary information.</p>
```

### Prose Container

For long-form content with optimal reading width:

```html
<article class="prose">
  <h2>Article Title</h2>
  <p>Long-form content with comfortable line length and spacing.</p>
  <blockquote>A meaningful quote.</blockquote>
  <ul>
    <li>List item one</li>
    <li>List item two</li>
  </ul>
</article>
```

---

## Buttons

### Variants

```html
<button class="btn btn-primary">Primary</button>
<button class="btn btn-secondary">Secondary</button>
<button class="btn btn-ghost">Ghost</button>
<button class="btn btn-danger">Danger</button>
```

### Sizes

```html
<button class="btn btn-primary btn-sm">Small</button>
<button class="btn btn-primary">Default</button>
<button class="btn btn-primary btn-lg">Large</button>
```

### States

```html
<button class="btn btn-primary" disabled>Disabled</button>
```

### Full Width

```html
<button class="btn btn-primary btn-block">Full Width</button>
```

### Icon Button

```html
<button class="btn btn-secondary btn-icon">
  <svg>...</svg>
</button>
```

### Button with Loading

```html
<button class="btn btn-primary" disabled>
  <span class="spinner spinner-sm"></span>
  Loading...
</button>
```

---

## Form Elements

### Text Input

```html
<div class="form-group">
  <label class="form-label">Label</label>
  <input type="text" class="input" placeholder="Placeholder">
  <span class="form-helper">Helper text</span>
</div>
```

### Required Field

```html
<label class="form-label form-label-required">Required Field</label>
<input type="text" class="input">
```

### Error State

```html
<div class="form-group">
  <label class="form-label">Email</label>
  <input type="email" class="input input-error" value="invalid">
  <span class="form-error">Please enter a valid email.</span>
</div>
```

### Success State

```html
<input type="text" class="input input-success" value="valid input">
```

### Select

```html
<select class="input select">
  <option>Choose option...</option>
  <option>Option 1</option>
  <option>Option 2</option>
</select>
```

### Textarea

```html
<textarea class="input textarea" placeholder="Message..."></textarea>
```

### Checkbox

```html
<label class="checkbox">
  <input type="checkbox">
  <span>Checkbox label</span>
</label>

<label class="checkbox">
  <input type="checkbox" checked>
  <span>Checked by default</span>
</label>
```

### Radio

```html
<label class="radio">
  <input type="radio" name="group1" checked>
  <span>Option A</span>
</label>
<label class="radio">
  <input type="radio" name="group1">
  <span>Option B</span>
</label>
```

### Toggle Switch

```html
<label class="toggle">
  <input type="checkbox">
  <span>Enable notifications</span>
</label>
```

---

## Cards

### Basic Card

```html
<div class="card">
  <div class="card-body">
    Simple card content.
  </div>
</div>
```

### Full Card

```html
<div class="card">
  <div class="card-header">
    <h3 class="card-title">Title</h3>
    <p class="card-description">Description text</p>
  </div>
  <div class="card-body">
    Main content area.
  </div>
  <div class="card-footer">
    <button class="btn btn-primary">Save</button>
    <button class="btn btn-ghost">Cancel</button>
  </div>
</div>
```

### Hover Card

```html
<div class="card card-hover">
  <div class="card-body">
    Lifts on hover.
  </div>
</div>
```

---

## Alerts

```html
<div class="alert alert-info">
  <div class="alert-content">
    <div class="alert-title">Info</div>
    <div class="alert-description">Informational message.</div>
  </div>
</div>

<div class="alert alert-success">
  <div class="alert-content">
    <div class="alert-title">Success</div>
    <div class="alert-description">Action completed.</div>
  </div>
</div>

<div class="alert alert-warning">
  <div class="alert-content">
    <div class="alert-title">Warning</div>
    <div class="alert-description">Proceed with caution.</div>
  </div>
</div>

<div class="alert alert-error">
  <div class="alert-content">
    <div class="alert-title">Error</div>
    <div class="alert-description">Something went wrong.</div>
  </div>
</div>
```

---

## Badges

```html
<span class="badge badge-default">Default</span>
<span class="badge badge-primary">Primary</span>
<span class="badge badge-success">Success</span>
<span class="badge badge-warning">Warning</span>
<span class="badge badge-error">Error</span>
<span class="badge badge-info">Info</span>
```

### With Dot

```html
<span class="badge badge-success badge-dot">Active</span>
<span class="badge badge-error badge-dot">Offline</span>
```

---

## Avatars

### Sizes

```html
<div class="avatar avatar-sm">S</div>
<div class="avatar">M</div>
<div class="avatar avatar-lg">L</div>
<div class="avatar avatar-xl">XL</div>
```

### With Image

```html
<div class="avatar">
  <img src="photo.jpg" alt="User name">
</div>
```

### Avatar Group

```html
<div class="avatar-group">
  <div class="avatar">A</div>
  <div class="avatar">B</div>
  <div class="avatar">C</div>
  <div class="avatar">+5</div>
</div>
```

---

## Tables

### Basic Table

```html
<table class="table">
  <thead>
    <tr>
      <th>Name</th>
      <th>Email</th>
      <th class="cell-numeric">Amount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John Doe</td>
      <td>john@example.com</td>
      <td class="cell-numeric">$100.00</td>
    </tr>
  </tbody>
</table>
```

### Variants

```html
<!-- Striped rows -->
<table class="table table-striped">...</table>

<!-- Hover effect -->
<table class="table table-hover">...</table>

<!-- With border -->
<div class="table-bordered">
  <table class="table">...</table>
</div>

<!-- Combined -->
<div class="table-bordered">
  <table class="table table-striped table-hover">...</table>
</div>
```

---

## Tabs

```html
<div class="tabs">
  <div class="tabs-list">
    <button class="tabs-trigger active">Tab 1</button>
    <button class="tabs-trigger">Tab 2</button>
    <button class="tabs-trigger">Tab 3</button>
  </div>
  <div class="tabs-content">
    <div class="tabs-panel active">Content 1</div>
    <div class="tabs-panel">Content 2</div>
    <div class="tabs-panel">Content 3</div>
  </div>
</div>
```

JavaScript required for interactivity:

```javascript
function switchTab(trigger, panelId) {
  document.querySelectorAll('.tabs-trigger').forEach(t => t.classList.remove('active'));
  document.querySelectorAll('.tabs-panel').forEach(p => p.classList.remove('active'));
  trigger.classList.add('active');
  document.getElementById(panelId).classList.add('active');
}
```

---

## Navigation

```html
<nav class="nav">
  <a href="/" class="nav-brand">Brand</a>
  <div class="nav-menu">
    <a href="#" class="nav-link active">Home</a>
    <a href="#" class="nav-link">About</a>
    <a href="#" class="nav-link">Contact</a>
  </div>
  <div class="nav-actions">
    <button class="btn btn-primary btn-sm">Sign Up</button>
  </div>
</nav>
```

### Breadcrumbs

```html
<nav class="breadcrumbs">
  <span class="breadcrumb-item"><a href="#">Home</a></span>
  <span class="breadcrumb-item">/</span>
  <span class="breadcrumb-item"><a href="#">Category</a></span>
  <span class="breadcrumb-item">/</span>
  <span class="breadcrumb-item">Current</span>
</nav>
```

---

## Modal

```html
<!-- Trigger -->
<button onclick="openModal()">Open Modal</button>

<!-- Backdrop -->
<div class="modal-backdrop" id="backdrop"></div>

<!-- Modal -->
<div class="modal" id="modal">
  <div class="modal-header">
    <h3 class="modal-title">Modal Title</h3>
    <button class="modal-close" onclick="closeModal()">×</button>
  </div>
  <div class="modal-body">
    Modal content goes here.
  </div>
  <div class="modal-footer">
    <button class="btn btn-ghost" onclick="closeModal()">Cancel</button>
    <button class="btn btn-primary">Confirm</button>
  </div>
</div>

<script>
function openModal() {
  document.getElementById('backdrop').classList.add('open');
  document.getElementById('modal').classList.add('open');
}
function closeModal() {
  document.getElementById('backdrop').classList.remove('open');
  document.getElementById('modal').classList.remove('open');
}
</script>
```

---

## Accordion

```html
<div class="accordion">
  <div class="accordion-item open">
    <button class="accordion-trigger">
      Question 1
      <span class="accordion-icon">▼</span>
    </button>
    <div class="accordion-content">
      <div class="accordion-content-inner">
        Answer 1
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <button class="accordion-trigger">
      Question 2
      <span class="accordion-icon">▼</span>
    </button>
    <div class="accordion-content">
      <div class="accordion-content-inner">
        Answer 2
      </div>
    </div>
  </div>
</div>

<script>
document.querySelectorAll('.accordion-trigger').forEach(trigger => {
  trigger.addEventListener('click', () => {
    trigger.parentElement.classList.toggle('open');
  });
});
</script>
```

---

## Lists

```html
<div class="list">
  <div class="list-item">
    <div class="avatar avatar-sm">JD</div>
    <div class="list-item-content">
      <div class="list-item-title">John Doe</div>
      <div class="list-item-description">Developer</div>
    </div>
    <span class="badge badge-success">Online</span>
  </div>
</div>

<!-- Interactive list -->
<div class="list list-interactive">
  <div class="list-item">Clickable item</div>
</div>
```

---

## Pagination

```html
<nav class="pagination">
  <button class="pagination-item" disabled>←</button>
  <button class="pagination-item active">1</button>
  <button class="pagination-item">2</button>
  <button class="pagination-item">3</button>
  <button class="pagination-item">→</button>
</nav>
```

---

## Loading States

### Spinner

```html
<span class="spinner spinner-sm"></span>
<span class="spinner"></span>
<span class="spinner spinner-lg"></span>
```

### Skeleton

```html
<div class="skeleton" style="height: 20px; width: 200px;"></div>
<div class="skeleton" style="height: 100px; width: 100%;"></div>
```

---

## Utilities

### Display

```html
<div class="block">Block</div>
<div class="flex">Flex</div>
<div class="grid">Grid</div>
<div class="hidden">Hidden</div>
```

### Flexbox

```html
<div class="flex flex-col gap-4">
  <div class="flex justify-between items-center">
    <span>Left</span>
    <span>Right</span>
  </div>
</div>
```

### Grid

```html
<div class="grid grid-cols-3 gap-4">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

### Spacing

```html
<!-- Margin -->
<div class="mt-4">Margin top 16px</div>
<div class="mb-8">Margin bottom 32px</div>
<div class="mx-auto">Centered horizontally</div>

<!-- Padding -->
<div class="p-4">Padding 16px all sides</div>
<div class="px-6 py-4">Padding x 24px, y 16px</div>
```

### Typography

```html
<p class="text-sm">Small text</p>
<p class="text-lg font-bold">Large bold</p>
<p class="text-muted">Muted color</p>
<p class="text-center">Centered</p>
<p class="truncate">Truncated with ellipsis...</p>
```

### Borders & Radius

```html
<div class="border rounded-lg">Bordered, rounded</div>
<div class="border-b">Bottom border only</div>
<div class="rounded-full">Fully rounded</div>
```

### Shadows

```html
<div class="shadow-sm">Small shadow</div>
<div class="shadow-md">Medium shadow</div>
<div class="shadow-lg">Large shadow</div>
```

---

## Customization

Override CSS variables in your stylesheet:

```css
:root {
  /* Colors */
  --primary: #2563eb;
  --primary-hover: #1d4ed8;
  
  /* Typography */
  --font-sans: 'Your Font', sans-serif;
  --text-base: 1rem;
  
  /* Spacing */
  --space-4: 1rem;
  
  /* Borders */
  --radius-md: 8px;
  --border-width: 2px;
  
  /* Shadows */
  --shadow-md: 0 4px 12px rgba(0,0,0,0.15);
}
```

### Targeting Themes

```css
[data-theme="light"] {
  --bg-page: #fafafa;
}

[data-theme="gentle"] {
  --bg-page: #f5f5f0;
}
```
