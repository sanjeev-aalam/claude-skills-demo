---
name: a11y-review
description: Review an HTML page for common accessibility issues
when_to_use: When the user asks to review a page, check accessibility, or audit a11y
allowed-tools: Read, Grep, Glob
---

Run a read-only accessibility review on the requested page.

Check every item below. For each issue found, report the line number, the element, what is wrong, and how to fix it.

## Checklist

### Images and media
- Every `<img>` has an `alt` attribute (descriptive for content images, `alt=""` for decorative)
- SVG images used as content have `role="img"` and an accessible name (`aria-label` or `<title>`)

### Headings
- Exactly one `<h1>` per page
- Heading levels do not skip (e.g., no `<h1>` followed by `<h3>`)

### Forms
- Every form input has a visible `<label>` with a matching `for`/`id` pair
- Required fields are marked with `required` or `aria-required`
- The form has a submit button

### Color and contrast
- Text is not distinguished by color alone
- CSS uses variables that can be themed for higher contrast

### Keyboard and focus
- Interactive elements (`<a>`, `<button>`, `<input>`) are natively focusable
- Custom interactive elements have appropriate ARIA roles
- Focus styles are visible (not removed with `outline: none` without replacement)

### Landmarks
- Page uses landmark elements: `<header>`, `<nav>`, `<main>`, `<footer>`
- There is exactly one `<main>` element

## Output format

List each issue as:

```
[ISSUE] Line XX — <element>
Problem: …
Fix: …
```

If no issues are found, say "No accessibility issues found."
