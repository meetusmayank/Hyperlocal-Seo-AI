# LOCAL Ai — Landing pages (HTML)

Two static pages, no build step:

- `index.html` — Overview landing page (Website SEO + Local SEO dashboard)
- `local-seo.html` — Local SEO start flow (search → pick business → scan → results)

## Run

Double-click `index.html`, or serve the folder with any web server (Netlify, Vercel, cPanel, S3, etc.).
Navigation: the **Hyperlocal** menu item and "Run a free local scan" button open `local-seo.html`.

## Structure

```
index.html
local-seo.html
assets/
  local-ai-logo.png
  css/index.css          styles for the overview page
  css/local-seo.css      styles for the Local SEO flow
  vendor/htm-preact-standalone.umd.js   tiny UI runtime (Preact + htm, ~13 KB, MIT)
```

Page markup and logic live in a `<script>` block inside each HTML file (the `template()` function holds the markup; `Component.renderVals()` holds the data and handlers).
Fonts load from Google Fonts (Plus Jakarta Sans, JetBrains Mono).

## Before going live

- All dashboard numbers, business matches and scan results are **sample data**.
- Hook up: audit form (`submitAudit`), client login (`submitLogin`), business search (Google Places) and directory scan API (`startScan`).
- Fill in the "Which countries are supported?" FAQ answer in `local-seo.html`.
