# Northwind Labs Website

A static marketing site — plain HTML, CSS and JavaScript, no build step.

## File layout

```
index.html          Home page
about.html          Team page
contact.html        Contact form
css/styles.css      All styles (mobile-first, CSS variables)
js/main.js          Mobile nav toggle
```

## Preview

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000 in a browser.

## Rules

1. **Semantic HTML** — use the right element (`<nav>`, `<main>`, `<section>`, `<article>`, `<label>`, etc.), not just `<div>`.
2. **Every `<img>` and SVG image must have alt text** — descriptive for content images, `alt=""` for purely decorative ones.
3. **No inline styles** — all styling goes in `css/styles.css`.
4. **Mobile-first CSS** — base styles target small screens; use `min-width` media queries for larger breakpoints.
5. **No frameworks or build tools** — vanilla HTML, CSS and JS only.
