# MidnightAviator196.github.io

## Overview

This is a static personal website project hosted on GitHub Pages. The site features multiple interactive pages including a home page, a real-time California timezone clock, and password-protected secret pages. It's built entirely with vanilla HTML, CSS, and JavaScript with Tailwind CSS for modern styling on some pages.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend-Only Architecture
- **Problem**: Need a simple personal website with interactive features
- **Solution**: Pure static site with HTML, CSS, and JavaScript - no backend required
- **Rationale**: GitHub Pages hosting only supports static files; client-side JavaScript handles all interactivity

### Page Structure
- `index.html` - Main landing page with navigation links
- `california_time.html` - Real-time clock using JavaScript's Intl API for timezone conversion
- `secreat.html` - Password-protected entry page with client-side authentication
- `secrete/` folder - Contains protected content pages (`secret_links.html`, `text.html`)

### Styling Approach
- **Hybrid styling**: Some pages use inline CSS (index.html, secreat.html), while others use Tailwind CSS via CDN (california_time.html)
- **No build process**: All CSS is either inline or loaded from CDN, keeping deployment simple

### Security Implementation
- **Client-side password protection**: JavaScript-based authentication on secret pages
- **Rate limiting**: Protection against brute-force attempts implemented in JavaScript
- **Referrer checking**: Protected content pages verify the user came from the correct entry point
- **Note**: This is security through obscurity only - not suitable for truly sensitive content

## External Dependencies

### CDN Resources
- **Tailwind CSS** (`https://cdn.tailwindcss.com`) - Utility-first CSS framework loaded via CDN on select pages

### External Links
- Google.com and Python.org linked from the home page
- Python logo image loaded from python.org's static resources

### Hosting
- **GitHub Pages** - Static site hosting (implied by repository name format)

### No Backend Services
- No database
- No server-side processing
- No API integrations
- All functionality runs in the browser