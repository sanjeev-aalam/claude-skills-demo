---
name: new-page
description: Add a new page to the Northwind Labs site with the shared header, footer and nav
when_to_use: When the user wants to add a new page, create a page, or asks about adding a page to the site
---

Add a new page to the Northwind Labs site. Follow every step below.

## Steps

1. Copy the page template from `references/page-template.html` as your starting point.
2. Fill in the `<title>` as "Page Name — Northwind Labs".
3. Fill in the `<meta name="description">` with a one-sentence summary.
4. Give the page exactly one `<h1>`.
5. Set `aria-current="page"` on the new page's nav link.
6. Remove `aria-current="page"` from whichever link had it in the template.
7. Save the file at the root of the project (e.g., `pricing.html`).
8. **Update every existing page** — add a nav `<li>` for the new page inside the `<ul class="nav-list">` in `index.html`, `about.html`, and `contact.html`.
9. Verify the new file opens correctly in a browser.

## Checklist

- [ ] Page has `<!DOCTYPE html>` and `lang="en"`
- [ ] `<meta charset>` and `<meta viewport>` present
- [ ] Title follows the pattern "Name — Northwind Labs"
- [ ] Exactly one `<h1>` on the page
- [ ] Nav link added to **all** pages
- [ ] `aria-current="page"` set correctly
- [ ] Footer matches other pages
- [ ] `js/main.js` script tag included
