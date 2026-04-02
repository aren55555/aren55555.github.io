# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a static personal portfolio/resume website for Aren Patel, hosted on GitHub Pages at `resume.arenpatel.com`. There is no build system, package manager, or test infrastructure — everything is plain HTML/CSS/JS deployed directly.

## Architecture

The site has two entry points:
- `index.html` — root redirect to `/resume`
- `resume/index.html` — the actual resume page (754 lines of HTML)

Bundled dependencies (not installed via package manager, just checked-in files):
- Bootstrap (CSS + JS) in `resume/css/` and `resume/js/`
- Font Awesome in `resume/font-awesome/`
- FancyBox jQuery plugin in `resume/fancybox/`
- jQuery v1.11.0 (loaded from a CDN in the HTML)

Custom styles live in `resume/styles.css`. All project images are in `resume/img/`.

## Deployment

Push to `main` branch → GitHub Pages auto-deploys. No CI/CD pipeline.

Custom domain is configured via the `CNAME` file (`resume.arenpatel.com`).

## Development

Open `resume/index.html` directly in a browser — no local server needed. For local preview with routing:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000/resume/`.
