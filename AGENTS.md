# Poster Design

## Overview

Minimal, single-page web app for creating interactive A3 posters with editable text, draggable circles, and color cycling. No build tools, no frameworks — pure HTML/CSS/JS served as a static file.

## Tech Stack

- **Vanilla HTML5, CSS3, JavaScript (ES6)** — everything in a single `index.html`
- **Interact.js** (CDN) — drag interaction for SVG circles
- **SVG** — A3 poster canvas (841.89 × 1190.55 pt)
- **Canvas API** — PNG export (SVG → canvas → download)

## Project Structure

```
poster-design/
├── index.html          # Entire application (~290 lines)
├── AGENTS.md           # This file
└── .gitattributes      # * text=auto (LF normalization)
```

## Key Features

1. **Live text editing** — 4 inputs update SVG text in real time (top text, two center words, bottom text)
2. **Circle dragging** — two white circles draggable via Interact.js, with `mix-blend-mode: difference`
3. **Color cycling** — scroll mouse wheel to cycle colors through HSL rainbow → white → black (applied to circles + text)
4. **PNG export** — button downloads poster as PNG (SVG serialized → canvas render → download)

## Dependencies

- Interact.js: `<https://cdn.jsdelivr.net/npm/interactjs/dist/interact.min.js>`
- Fonts (must be installed locally): DrukCondTrial-Super, DrukCondTrial-SuperItalic

## No Build / No Tests

No package.json, no linting, no testing setup. Open `index.html` directly in a browser to run.

## Conventions

- UI labels in Italian (e.g., "Poster Interattivo - Generatore")
- `.cls-2` = circles, `.cls-3` = top/bottom text, `.cls-4` = center text (huge, italic)
- Control panel has glassmorphism style (`backdrop-filter: blur`)
- Git remote: `https://github.com/Remo1112/poster-design.git`

## Git History

- `6ab860a` — Update index.html
- `2a86eb0` — Creato progetto
- `1dcc8d4` — Initial commit
