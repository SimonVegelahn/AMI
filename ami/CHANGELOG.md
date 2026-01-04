# Changelog

All notable changes to AMI Design System will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [3.0.0] - 2025-01-04

### Added
- **Eye-Gentle Theme** — New `data-theme="gentle"` option with reduced contrast, warmer whites, and slightly larger text for extended reading sessions
- **Dark Section Modifier** — `.section-dark` class for opt-in dark regions within light pages
- **AAA Contrast for Interactive Elements** — Navigation, buttons, and form labels now meet WCAG AAA (7:1+) contrast requirements
- **Semantic Color Tokens** — New `--text-interactive`, `--text-nav` tokens for consistent accessible interactive text
- **Touch Target Compliance** — All interactive elements meet 44px minimum touch target size
- **Accordion Component** — Collapsible content sections with smooth animations
- **Empty State Component** — Styled placeholder for empty lists/tables
- **Skeleton Loader** — Shimmer animation for loading states

### Changed
- **Typography System** — Serif body text (Source Serif 4) for warmth, sans-serif (Inter) for headings/UI
- **Border Radius** — Increased default radius from 2-4px to 4-6px for friendlier appearance
- **Primary Color** — Shifted from blue to indigo for better contrast ratios
- **Shadow System** — Softer, more subtle shadows throughout
- **Focus States** — More visible focus rings with configurable offset

### Fixed
- Button text contrast now AAA compliant on all variants
- Form input placeholder contrast meets AA requirements
- Table header contrast improved for readability

### Removed
- Dark theme as default (now light-first, dark via modifier only)
- Overly saturated color variants

---

## [2.0.0] - Previous Local Version

### Added
- Component library (buttons, forms, cards, alerts, badges)
- Utility classes for layout and spacing
- CSS custom properties for theming
- Basic accessibility features

### Notes
- This version was maintained locally and not publicly released

---

## [1.0.0] - Initial Local Version

### Added
- Initial token system
- Basic reset styles
- Core components

### Notes
- Internal use only
