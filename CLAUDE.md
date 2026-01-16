# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static portfolio website for a UX designer. Single-page application with full-screen scrollable sections, built with vanilla HTML, CSS, and JavaScript (no build tools or frameworks).

## Development

Open `index.html` directly in a browser - no server or build step required.

To test locally with a server (for features that require HTTP):
```bash
python3 -m http.server 8000
# or
npx serve .
```

## Architecture

- **index.html** - Single HTML file with all sections (Hero, Portfolio, Experience, About, Contact) and semantic structure with ARIA attributes
- **styles.css** - All styling including CSS custom properties (`:root` variables), responsive breakpoints, and animations. Color scheme defined at top of file
- **script.js** - All interactivity: navigation, portfolio modals, form validation, and intersection observer animations. Project data for modals stored in `projectData` object at top

## Key Configuration Points

- **Contact form**: Uses Web3Forms API. Replace `YOUR_WEB3FORMS_ACCESS_KEY_HERE` in script.js (~line 404) with actual key from web3forms.com
- **Resume download**: Update the `downloadBtn` click handler in script.js (~line 343-354) with actual resume URL
- **Color theming**: CSS custom properties in `:root` selector at top of styles.css

## Responsive Breakpoints

- 1024px: Tablet layouts
- 768px: Mobile navigation toggle
- 480px: Small mobile adjustments
