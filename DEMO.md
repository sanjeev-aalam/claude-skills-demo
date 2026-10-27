# Demo Script — Claude Code Project Configuration

## Planted accessibility issues in contact.html

Three subtle, realistic a11y bugs have been planted in `contact.html`:

1. **Missing image alt text** — The office illustration SVG (line ~66) has no `role="img"` or `alt`/`aria-label` attribute, making it invisible to screen readers.
2. **Skipped heading level** — The page goes from `<h1>` ("Get in touch") straight to `<h3>` ("Send us a message"), skipping `<h2>`.
3. **Missing form label** — The email input has a `placeholder` but no `<label>` element, so screen readers cannot identify the field.

## 2-minute demo script

### 1. Commit-message skill

There is a staged change (a "Back to top" link added to every page footer).

> **Prompt:** "write a commit message for my staged changes"

Claude Code will use the `commit-message` skill to read the staged diff and produce a Conventional Commits message.

### 2. New-page skill

> **Prompt:** "add a new page called pricing"

Claude Code will use the `new-page` skill to scaffold `pricing.html` from the template, add the nav link to all existing pages, and set `aria-current="page"`.

### 3. Accessibility review skill

> **Prompt:** "review contact.html for accessibility"

Claude Code will use the `a11y-review` skill (which is limited to read-only tools) and should find all three planted issues: the missing image alt text, the skipped heading level, and the missing form label.
