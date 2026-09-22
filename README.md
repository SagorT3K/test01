# test01

A single-file static landing page — plain HTML + CSS, no framework, no build step, no dependencies.

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](https://developer.mozilla.org/docs/Web/CSS)
[![No JavaScript](https://img.shields.io/badge/JavaScript-none-lightgrey?style=flat-square)](.)
[![No build step](https://img.shields.io/badge/build-none-success?style=flat-square)](.)

## Overview

[`index.html`](index.html) is a complete, responsive one-page marketing site with every style inlined in a single `<style>` block. It is meant as a starting template for a landing page — and as a throwaway page for testing hosting setups (static hosts, reverse proxies, CDNs) where you just need *a* page to serve.

Sections, top to bottom:

| Section | Content |
| --- | --- |
| Sticky navbar | Gradient header, `test01` logo, anchors to Features / About / Contact |
| Hero | Full-viewport gradient hero with headline, sub-text, **Get Started** / **Learn More** buttons and a decorative circle |
| Features | Six-card grid: Lightning Fast, Secure & Reliable, Fully Responsive, Beautiful Design, Easy Integration, Great Support (emoji icons) |
| About | Two-column text block next to a `Your Image Here` placeholder |
| Stats | Four metric tiles: 10K+ Active Users · 99.9% Uptime · 150+ Countries · 24/7 Support |
| CTA | "Ready to Get Started?" band with a **Start Free Trial** button |
| Footer | Product / Company / Support link columns and a `© 2024 test01` copyright line |

Everything — headings, metrics, feature copy, prices, links — is placeholder content. There is no JavaScript at all: the sticky navbar, hover states, card lift and gradient backgrounds are pure CSS.

## Run it

No install step. Either open the file directly:

```bash
start index.html        # Windows
open index.html         # macOS
```

or serve the folder (closer to how a host will serve it):

```bash
python -m http.server 8000   # http://localhost:8000
npx serve .                  # alternative, if Node is installed
```

## Deploy

Any static host works, because there is nothing to build. For GitHub Pages: push this repository, then **Settings → Pages → Deploy from a branch → `main` / `(root)`** — no build command, no output directory.

## Customizing

- **Copy** — edit the markup in `<body>`; the sections are separated by `<!-- ... -->` comments.
- **Theme** — the two `linear-gradient(135deg, #667eea 0%, #764ba2 100%)` values drive the navbar, hero and CTA backgrounds; per-section colors live in the `<style>` block right above each section's rules.
- **Layout** — the grid/max-width breakpoints are in the `@media` rules at the end of the `<style>` block.
- **Navbar links** — the `#features` and `#about` anchors resolve; the Contact link points at `#contact`, but no element carries that id yet, so add a contact section (or repoint the link) when you reuse the template.

## Project structure

```
test01/
└── index.html      the entire site (markup + styles)
```

## Notes

- No license file is included — add one before reusing this template publicly.
- With no JS and no tooling there is nothing to install, lint or test; a hard refresh is the whole development loop.
