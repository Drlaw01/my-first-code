## Repository snapshot

This repo is a tiny static website containing three HTML pages at the repository root:
- `index.html`
- `My Corriculum Vitae.html` (note: spelling & filename contains spaces)
- `New.html`

There is no build system, test harness, or CI configured in the repository.

## What to know (big-picture)

- This is a purely static front-end repository — edits are limited to plain HTML files. There are no JavaScript frameworks, package.json, or backend services to consider.
- The most important files to inspect and change are the three HTML files listed above. Fixes should be small, single-responsibility edits that improve markup validity and consistency.

## Common / recurring patterns you will act on

- Incorrect or inconsistent HTML casing: tags like `Html`, `Head`, and `Body` appear in different cases — normalize to lowercase (e.g., `<html>`, `<head>`, `<body>`).
- Doctype and invalid doctype usage: some files have `<! doctype html>` (space) — change to `<!DOCTYPE html>`.
- Missing or malformed tags: several files are missing proper opening/closing tags (e.g., `<html>` or `</html>`). Close all tags and ensure valid nesting.
- Filenames and spelling: filenames contain spaces and there are spelling errors (`My Corriculum Vitae.html` should be `My Curriculum Vitae.html`). Prefer filenames without spaces and with correct spelling when creating or renaming files.

## Editing recommendations (actionable examples)

- When fixing `index.html`:
  - Replace `<! doctype html>` with `<!DOCTYPE html>`.
  - Ensure tag casing is consistent and all tags are closed.

- When fixing `My Corriculum Vitae.html`:
  - Correct the filename spelling (no spaces if possible) and close any missing `</html>`.
  - Keep content changes minimal unless the user asked for a content update.

- When fixing `New.html`:
  - Remove stray/invalid tokens like `Html>` and close all unclosed tags (e.g., the `<ul>` and `<h4>` in this file).

## How to test your changes locally

- A browser is the expected test environment — open the edited HTML files directly or serve them locally with a simple static server. Example commands you can use in PowerShell (Windows):

```powershell
# If you have Python installed
python -m http.server 8000

# Or, if you have Node.js and http-server installed globally
npx http-server -p 8000
```

- You can also validate markup with the W3C HTML Validator (https://validator.w3.org/) or use an editor/IDE HTML linter.

## Conventions to follow

- Keep edits small and focused — one logical fix per commit with a short descriptive commit message (e.g., `fix(html): normalize doctype and close tags in New.html`).
- Preserve existing textual content unless the change is a straightforward bug fix (spelling or malformed tags). When in doubt, ask for clarification.

## When to propose bigger changes

- Add or suggest a README.md or basic CI if the repo owner asks for a development workflow.
- Recommend renaming files to remove spaces only after confirming with the repository owner or in an issue/PR description.

If anything in this guidance is unclear or you want the file to be more/less strict (e.g., automatic filename renames or larger refactors), tell me and I'll iterate.
