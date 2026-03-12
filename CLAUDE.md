# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static personal portfolio website for Johnny Kress. No build tools, frameworks, or package managers — just vanilla HTML, CSS, and JavaScript served directly from the filesystem or any static host.

To preview: open `index.html` in a browser, or use any static file server (e.g., `npx serve .` or VS Code Live Server).

## File Structure

- `index.html` — single-page site; all sections live here (About, Projects, Skills, Activities, Contact)
- `css/style.css` — all styles; uses CSS custom properties defined in `:root`
- `js/main.js` — scroll-based nav highlight, scroll fade-in via IntersectionObserver, nav shrink on scroll
- `Kress Resume.pdf` — source of truth for bio, projects, skills, and experience content

## Design System

Defined in `css/style.css` `:root`:
- **Accent color**: `--color-accent: #eab308` (yellow)
- **Backgrounds**: `--color-bg: #0a0a0a`, `--color-surface: #111111`, `--color-surface-alt: #161600`
- **Max content width**: `--max-width: 680px` (narrow, centered layout)
- **Fonts**: `--font-sans` for body, `--font-mono` for labels/tags/logo

## Adding Content

**New project card** — duplicate a `.card` block in the Projects section of `index.html`. Cards use `.card-image`, `.card-body`, `.card-title`, `.card-desc`, `.card-tags` (each item is a `.tag` span), and `.card-links`.

**New skill group** — duplicate a `.skill-group` div in the Skills section.

**New nav link** — add an `<li><a href="#section-id">Label</a></li>` to `.nav-links` and ensure the target section has a matching `id`.

**Scroll fade-in** — `main.js` automatically observes `.card`, `.skill-group`, and `.about-grid` elements. Any new section content using those classes will animate in automatically.

## Contact Info

- Email: Johnnykress808@gmail.com
- GitHub and LinkedIn URLs in the Contact section are placeholder `#` links and need to be filled in.
- Resume download links to `Kress Resume.pdf` in the project root.



