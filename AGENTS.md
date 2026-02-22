# AGENTS.md - Portfolio Website Guidelines

## Project Overview

This is a **static HTML/CSS portfolio website** for Elvin Cooper, a Software Developer specializing in Python, Flask, Oracle SQL, and backend development. The site showcases skills, experience, education, and projects.

**Tech Stack:**
- HTML5
- CSS3 (custom styles + Bootstrap 5.3 from CDN)
- Font Awesome 6.5.1 (icons)
- Google Fonts (Poppins)
- No JavaScript framework / No build system

---

## Build / Development Commands

This is a **static site** - no build commands required.

### Running Locally

Simply open `index.html` in a browser, or use a simple HTTP server:

```bash
# Python
python -m http.server 8000

# Or with PHP (if available)
php -S localhost:8000
```

### No Linting/Testing

This repository contains **only static HTML/CSS** - there are no:
- JavaScript/TypeScript files to lint
- Test suites
- Build processes

For the Python projects mentioned in the portfolio (Flask APIs), refer to their individual repositories.

---

## Code Style Guidelines

### HTML

1. **Document Structure**
   - Use semantic HTML5 elements (`<header>`, `<main>`, `<section>`, `<article>`, `<footer>`)
   - Always include `<!DOCTYPE html>` and `lang` attribute
   - Include meta tags for charset, viewport, and description

2. **Indentation**
   - 2 spaces per indentation level
   - No tabs

3. **Attributes**
   - Use double quotes for attribute values
   - Self-closing tags should not have trailing slash (e.g., `<img>` not `<img/>`)
   - Order: `id`, `class`, `src`/`href`, `alt`, `aria-*`, `data-*`

4. **Accessibility**
   - Always include `alt` attributes on images
   - Use semantic elements for navigation (`<nav>`, `<ul>`)
   - Include `aria-label` on icon-only buttons/links

### CSS

1. **Organization**
   - Use CSS custom properties (variables) for colors and sizes
   - Group related styles logically (e.g., all header styles together)
   - Put generic styles before specific ones

2. **Naming Conventions**
   - Use BEM-like naming: `.block__element--modifier`
   - Use descriptive class names (e.g., `.experience-item` not `.exp1`)

3. **Formatting**
   - One selector per line
   - Properties on separate lines
   - 2 spaces indentation
   - Include units (px, rem, em) - use `rem` for fonts

4. **Responsive Design**
   - Use `clamp()` for fluid typography
   - Use media queries for breakpoints (match Bootstrap: 576px, 768px, 992px, 1200px)
   - Mobile-first approach

### General

1. **File Organization**
   ```
   /
   ├── index.html      # Main HTML file
   ├── styles.css     # All custom CSS
   ├── CV/            # Resume PDFs
   ├── imagenes/      # Images
   └── .idea/         # IDE config (do not modify)
   ```

2. **External Resources**
   - CDN links should use stable versions (e.g., Bootstrap 5.3.3)
   - Include integrity hashes for CDN resources when possible

3. **Images**
   - Optimize images before adding (WebP preferred)
   - Use relative paths for local images
   - Always specify width/height to prevent layout shift

---

## Git Workflow

1. Create a branch for changes: `git checkout -b fix/description`
2. Make changes and commit: `git commit -m "Description of changes"`
3. Push and create PR if needed
4. Keep commits atomic and descriptive

---

## Common Tasks

### Adding a New Project Section

1. Add a new `<article class="experienceItem">` inside the `#proyectos` section
2. Include: title, tech badges, description, images, GitHub link, live demo link
3. Add matching CSS styles if needed

### Updating the Stack

1. Find the `#stack` section in `index.html`
2. Add new technology to appropriate column
3. Use Font Awesome icons (`<i class="fab fa-python"></i>`)

### Modifying Styles

1. Edit `styles.css`
2. Use CSS variables in `:root` for reusable values
3. Test responsive behavior at different breakpoints

---

## External Project References

The portfolio mentions several Python/Flask projects hosted on GitHub:
- `ElvinCooper/Inventario-Docker` - Inventory API
- `ElvinCooper/api_noticias` - News API (InfoNovaX)
- `ElvinCooper/-Contact_api` - Contact Management API

These have their own repositories with proper CI/CD, testing, and Python code standards.
