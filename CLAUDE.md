# Varner Lab Website

## Overview
- Academic research lab website for Jeffrey D. Varner at Cornell University
- Hosted on **GitHub Pages** at `varnerlab.github.io`
- Custom domain: **varnerlab.org** (DNS via Network Solutions, CNAME file in repo)
- HTTPS enforced via GitHub Pages

## Tech Stack
- Static site: plain HTML + CSS (no frameworks, no build step)
- Single `style.css` for all pages
- No JavaScript dependencies

## Pages
- `index.html` — Home (bio, research areas, lab overview)
- `publications.html` — Publications
- `software.html` — Software/tools
- `teaching.html` — Teaching
- `experimental.html` — Experimental

## Structure
- Shared navbar across all pages (manually duplicated, not templated)
- `favicon.svg` for site icon
- `CNAME` file for custom domain routing
