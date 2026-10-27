---
name: commit-message
description: Write a git commit message in Conventional Commits format for the currently staged changes
when_to_use: When the user asks for a commit message, commit summary, or help committing
---

Write a commit message for the staged changes following these rules:

1. **Format:** `type(scope): summary`
2. **Types:** feat, fix, docs, style, refactor, test, chore, build, ci, perf
3. **Scope:** the area of the codebase affected (e.g., `css`, `nav`, `contact`, `about`)
4. **Summary line:** present tense, lowercase, no period, under 72 characters
5. **Body (optional):** separated by a blank line, wrap at 72 characters, explain *why* not *what*

Steps:

1. Run `git diff --cached --stat` to see which files are staged.
2. Run `git diff --cached` to read the actual changes.
3. Pick the most accurate type and scope.
4. Write a summary that describes the intent of the change.
5. Add a body only if the *why* is not obvious from the summary.
6. Present the full commit message in a code block so the user can copy it.
