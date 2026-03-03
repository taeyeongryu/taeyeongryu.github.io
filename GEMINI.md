# GEMINI.md

This file provides foundational mandates and context for Gemini CLI when working in this repository.

## Project Overview

Static portfolio website for **Taeyeong Ryu**, hosted via GitHub Pages at [taeyeongryu.github.io](https://taeyeongryu.github.io). It is built using pure HTML/CSS without any build tools, bundlers, or JavaScript frameworks.

- **Primary Language:** Korean (lang="ko")
- **Tech Stack:** HTML5, CSS3 (Vanilla)
- **Hosting:** GitHub Pages (serves from the `main` branch)

## Architecture & Directory Structure

- `/index.html`: Single-page site with sections: hero, about, skills, projects, contact.
- `/style.css`: All styles; uses CSS custom properties, CSS Grid for layouts, and is responsive at 600px breakpoint.
- `/resume/index.html`: A detailed, professional resume page.
- `/resume/style.css`: Specific styling for the resume layout.
- `/resume/profile.jpg`: Profile image used in the resume.

## Development Workflow

### Running Locally
No build step required. Open `index.html` directly in a browser or use a simple local server:
```powershell
# Using Python
python -m http.server 8000
```

### Git Workflow
- **`main` branch:** Production/deployment branch. GitHub Pages serves from here.
- **`dev` branch:** Active development branch.
- **Deployment:** Merge `dev` → `main` when ready to deploy.

## Engineering Standards & Conventions

### CSS Conventions
- **Design Tokens:** Defined as CSS custom properties in `:root` (`--primary`, `--accent`, `--bg`, `--bg-alt`, `--text`, `--text-light`).
- **Naming:** BEM-like class naming with simple descriptive names (e.g., `.skill-card`, `.project-grid`, `.nav-link`).
- **Layout:** Max content width is 900px.
- **Header:** Fixed header with backdrop blur.

### Content Updates
- Most content is static HTML.
- The resume includes a small inline script to calculate "Career Duration" dynamically.
- When adding new projects or skills, ensure consistency with existing card structures.

## Core Mandates for Gemini CLI
- **Preserve Korean Language:** All user-facing content should remain in Korean unless explicitly requested otherwise.
- **No Build Tools:** Do not introduce npm, Webpack, Vite, or other build-time dependencies. Keep the project as a pure static site.
- **Surgical Edits:** Maintain existing BEM-like class structure and CSS variable usage.
