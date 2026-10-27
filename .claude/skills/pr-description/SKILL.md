---
name: pr-description
description: Write a pull request description using the Northwind Labs PR template
when_to_use: When the user asks for a PR description, pull request description, or help writing a PR
---

Write a pull request description using the template below.

## How to fill it in

1. Run `git log --oneline main..HEAD` (or compare against the base branch) to understand all commits.
2. Run `git diff main..HEAD --stat` to see the full scope of changes.
3. Fill in every section of the template. Be specific — reviewers should understand the change without reading the diff.

## Template

```markdown
## Summary

One or two sentences explaining what this PR does and why.

## Changes

- Bullet list of meaningful changes
- Group related changes together
- Mention files or areas affected

## How to test

1. Step-by-step instructions a reviewer can follow
2. Include the preview command if relevant: `python3 -m http.server 8000`
3. Describe what correct behaviour looks like

## Screenshots

> Attach before/after screenshots for any visual change.
> Write "No visual changes" if not applicable.

## Risks

- Call out anything that might break
- Mention browser-compatibility concerns
- Write "Low risk" if the change is straightforward
```
