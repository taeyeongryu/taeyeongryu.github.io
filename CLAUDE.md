# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static portfolio website for Taeyeong Ryu, hosted via GitHub Pages at `taeyeongryu.github.io`. Pure HTML/CSS with no build tools, bundlers, or JavaScript frameworks.

## Architecture

- `index.html` — Single-page site with sections: hero, about, skills, projects, contact
- `style.css` — All styles; uses CSS custom properties (`:root` variables) for theming, CSS Grid for layouts, responsive at 600px breakpoint

The site is written in Korean (lang="ko").

## Development

No build step. Open `index.html` directly in a browser or use any local server (e.g., `python -m http.server`).

## Git Workflow

- `main` branch is the production/deploy branch (GitHub Pages serves from here)
- `dev` branch is used for development
- Merge `dev` → `main` when ready to deploy

## CSS Conventions

- Design tokens defined as CSS custom properties in `:root` (`--primary`, `--accent`, `--bg`, `--bg-alt`, `--text`, `--text-light`)
- BEM-like class naming with simple descriptive names (e.g., `.skill-card`, `.project-grid`, `.nav-link`)
- Max content width: 900px
- Fixed header with backdrop blur
