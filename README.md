<div align="center">

<img src="./assets/banner.svg" alt="Polished Dynamic Resume Builder" width="100%">

<br>

# Polished Dynamic Resume Builder

**A pure client-side application for generating and exporting structured, multi-template resumes using raw HTML and CSS.**

<img src="./assets/license.svg" alt="MIT License">

</div>

## Overview

A browser-based resume builder that stores resume information as structured JSON state and dynamically renders it into a variety of visual templates using native DOM APIs. Everything runs entirely within `index.html`.

### What it does

It provides a user interface to input personal details, experience, education, skills, and certifications. This data updates a central state object. A render function takes this state, selects a layout template, and outputs HTML directly into a preview canvas. The canvas is then scaled to fit a fixed A4 page proportion for native browser PDF export.

### Why it exists

To provide a simple, zero-dependency method for generating polished resumes without requiring external APIs, backend services, or complex build pipelines.

## Architecture

The application is built without virtual DOMs or external frameworks. It uses vanilla JavaScript to bind form inputs to a central state, which triggers a complete re-render of the template string upon modification.

<div align="center">
  <img src="./assets/architecture.svg" alt="Architecture Diagram" width="100%">
</div>

## Data Flow

Data moves from user input directly into the central state, which triggers a synchronous string-based HTML generation cycle.

<div align="center">
  <img src="./assets/dataflow.svg" alt="Data Flow Diagram" width="100%">
</div>

## Templates

The rendering engine supports 18 distinct templates, each defining its own layout, typography, and visual density. The available templates are:

- **classic**: Centered header, clean traditional layout.
- **modern**: Flexbox-based with a colored left sidebar and white main column.
- **minimal**: Left-aligned, two-column sections with minimalist typography.
- **professional**: Thick top border with shaded section headers.
- **creative**: High-contrast colored sidebar with a bright layout.
- **executive**: Centered, uppercase heavy typography for a commanding presence.
- **tech**: Courier/monospace fonts, dark accents, terminal-like section headers.
- **claude**: Elegant serif typography with italicized section headers.
- **swiss**: Lowercase, heavy weights, strictly right-aligned two-column grid.
- **infographic**: Sidebar layout featuring timeline icons and skill progress bars.
- **dashboard**: A card-based grid layout using CSS multi-column properties.
- **min-info**: Massive text with dot trackers for skill proficiencies.
- **max-info**: Dark mode, high contrast, blocky layouts with heavy borders.
- **art-info**: Blob shapes background with a clean timeline layout.
- **art-info-0**: Brutalist aesthetic with thick solid borders.
- **art-info-4**: Glassmorphism with blurred circles and semi-transparent panels.
- **comic**: Comic book style featuring rotated elements, thick borders, and heavy drop shadows.
- **art-info-2**: Data-heavy layout featuring CSS-rendered pie and bar charts.

## Layout System

The layout engine uses standard CSS. Depending on the template, it utilizes:
- **Flexbox** (`display: flex`) for sidebars, headers, and linear flows.
- **CSS Grid** (`display: grid`) for specific component alignments.
- **CSS Multi-column** (`column-count: 2`) to distribute content across available columns in templates like `dashboard` and `max-info`.

There is no virtual DOM or masonry engine; layout is purely handled by the browser's CSS renderer. 

## Technology

- **HTML5**: Structure and DOM container.
- **CSS3**: Variables, Flexbox, Grid, Multi-column layout, and Print Media Queries.
- **Vanilla JavaScript**: State management, event handling, and template literal rendering.
- **GitHub API**: (Optional) Fetches public repositories for project inclusion.
- **Google Fonts**: Typography system.

## Project Structure

```
project/
├── index.html
├── assets/
│   ├── architecture.svg
│   ├── banner.svg
│   ├── dataflow.svg
│   └── license.svg
└── README.md
```

## Quick Start

No installation, build step, or local server is required. 

1. Clone or download the repository.
2. Open `index.html` directly in any modern web browser.

## Usage

1. Fill out your information using the controls pane on the left.
2. Add your GitHub username to optionally fetch public repositories.
3. Select a template, font pair, and accent color.
4. Preview the rendering in real-time on the right.
5. Click **Save** to persist the JSON state locally via `localStorage`.

## PDF Workflow

The application does not use external PDF generation services (like Puppeteer or wkhtmltopdf). 

Instead, a custom JavaScript function (`UI.fitToPage`) uses `transform: scale()` to uniformly shrink the rendered resume until it fits precisely within a fixed `210mm` x `297mm` A4 container. Export is achieved entirely using the browser's native `window.print()` functionality, ensuring the PDF precisely matches the scaled preview.

## Design Principles

- **Zero dependencies**: No `npm install`, no bundlers.
- **Single Source of Truth**: `app.state` drives everything.
- **Predictable Output**: The layout strictly conforms to A4 dimensions before invoking the print dialog.

## Browser Compatibility

Compatible with modern browsers supporting ES6, CSS Flexbox/Grid, and `window.print()`. Tested primarily in Chromium-based browsers (Chrome, Edge) for reliable print-to-PDF output.

## License

This project is licensed under the MIT License.

---
*Built entirely with client-side web technologies.*
