# Timeline Visualizer

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-Single%20File-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=black)](https://reactjs.org/)
[![Built with AI](https://img.shields.io/badge/Built%20with-Claude%20AI-D4A574?logo=anthropic&logoColor=white)](https://claude.ai)

A pivot-based timeline visualization tool — plot activities across dynamic dimensions and switch perspectives instantly. Not a project management tool, but a fast visual thinking aid for temporal planning.

## Live Demo

**[https://runter-vom-mattenwagen.github.io/timeline-visualizer/](https://runter-vom-mattenwagen.github.io/timeline-visualizer/)**

## What It Does

Define **dimensions** (people, services, stages, workstreams — or anything you need), create **activities** with date ranges, assign them to dimensions, then pivot the view:

- **Lanes** = which dimension forms the rows
- **Color** = which dimension colors the bars

Same data, different perspectives. See who does what when, or which service moves through which stage when, or which workstream overlaps with which — just by switching two dropdowns.

### Example Use Cases

- **Data center migration**: Services × Stages × People — see per-person workload, per-stage timeline, or per-service schedule
- **Service buildout**: Workstreams × Activities — overlay parallel tracks to spot conflicts and dependencies
- **Event planning**: Venues × Teams × Days — visualize resource allocation across time

## Features

- **Dynamic Dimensions** — Create, rename, delete any number of dimensions
- **Multi-Project** — Switch between independent timelines
- **Calendar Weeks** — ISO week numbers in the header
- **Milestones** — Vertical red marker lines with labels
- **Dark / Light Mode** — Follows `prefers-color-scheme`, exports always light
- **Sticky Lane Labels** — Row names stay visible while scrolling horizontally
- **Fixed Legend Bar** — Color legend stays visible while scrolling
- **Undo / Redo** — Ctrl+Z / Ctrl+Shift+Z with 50-step history
- **Clone Activities** — Duplicate and modify in one step
- **Date Validation** — End date can never precede start date
- **Collapsible Sidebar** — Sections remember their open/closed state
- **Export** — SVG (vector), PNG (2× retina), JSON (single project or all)
- **Import** — Merge into existing projects or replace all, with preview
- **Zero Backend** — Everything in `localStorage`, single HTML file

## Tech Stack

- React 18 (via Babel standalone — no build step)
- SVG rendering for the timeline (no canvas, no charting library)
- Vanilla CSS with custom properties (light + dark theme)
- Data in browser `localStorage`

## Usage

Open `index.html` in any modern browser. No server, no install, no build.

### Data Backup

- **Export** → dropdown in toolbar, choose JSON (current project or all)
- **Import** → choose JSON file, preview contents, merge or replace

## Deployment

The repo is configured for GitHub Pages. The `index.html` in the root is served directly.

For self-hosting, drop the file into any web server's document root — it's fully self-contained.

## Built with AI

This project was built entirely with [Claude](https://claude.ai) by Anthropic — architecture, implementation, and iterative refinement through conversation. Every feature was designed, coded, and debugged in a single chat session.

## License

MIT — see [LICENSE](LICENSE)
