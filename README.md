# Augment Factory

A tiny static web app for building custom game "augment" cards — form on the left, live card preview on the right, saved library in `localStorage`, PNG export.

**Live:** https://juanledesmaa.github.io/augment-factory/

## Features

- Live preview while you type (title, effect, description, footnote)
- Three rarities with animated holographic frames: Prismatic, Gold, Silver
- Custom icon upload (stored with the card as a data URL)
- Save / update / edit / delete cards — persisted in the browser via `localStorage`
- Export the current card as a 2× PNG, or export the whole library at once

## Running locally

No build step, no dependencies to install. Serve the folder:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000. (Opening `index.html` directly via `file://` mostly works, but a local server avoids browser restrictions on image export.)

## Files

- `index.html` — the whole app (markup, styles, logic)
- `augment-icon.png` — default card icon
- `.github/workflows/pages.yml` — deploys the repo root to GitHub Pages on push

## Deployment

Pushing to the deploy branch runs the workflow above, which publishes the repo root to GitHub Pages. In the repository's **Settings → Pages**, the source must be set to **GitHub Actions**.
