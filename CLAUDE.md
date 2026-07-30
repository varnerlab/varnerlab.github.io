# Varner Lab Website

## Overview
- Academic research lab website for Jeffrey D. Varner at Cornell University
- Hosted on **GitHub Pages** at `varnerlab.github.io`
- Custom domain: **varnerlab.org** (DNS via Network Solutions, CNAME file in repo)
- HTTPS enforced via GitHub Pages

## Tech Stack
- Static site: plain HTML + CSS (no frameworks, no build step)
- Page styling lives in **inline `style="..."` attributes**, not a shared stylesheet
- `theme.css` holds the color tokens (the only shared stylesheet); no JS dependencies

## Colors & dark mode
- Every color in the HTML resolves through a `var(--token)` defined in `theme.css` —
  do not reintroduce hard-coded hex values in the pages
- Light values are the original palette; dark values are the counterpart. The dark
  block appears **twice** (under `prefers-color-scheme: dark` so it works without JS,
  and under `[data-theme="dark"]` so the nav toggle can override the system) — the two
  lists must stay identical
- The footer is dark in both themes and uses its own `--footer-*` tokens
- Each page has a small inline `<head>` script: applies the saved theme before first
  paint (no flash) and defines `toggleTheme()` for the nav button (`.themetog`)

## Pages
- `index.html` — Home (bio, research areas, lab overview)
- `publications.html` — Publications
- `software.html` — Software/tools
- `teaching.html` — Teaching
- `experimental.html` — Experimental

## Structure
- Shared navbar across all pages (manually duplicated, not templated) — the theme
  toggle button is the last item in the nav link row, so nav edits must touch all pages
- `favicon.svg` for site icon
- `CNAME` file for custom domain routing
