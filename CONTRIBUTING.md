# Contributing

This repository is a documentation archive for certifications, coursework certificates, and recognitions.

## Workflow

1. Add files under the correct provider or institution directory.
2. Update the closest provider-level `README.md` if one exists.
3. Update the root `README.md` in the same change so the main index stays current.
4. Use a focused Conventional Commit such as `docs: add coursera certificate for <course>`.

## Content Standards

- Treat the root `README.md` as the primary public index.
- Group entries by platform first, then by institution where appropriate.
- Include the certificate title and a public share link when one exists.
- Prefer additive edits; do not rewrite older entries unless you are fixing a broken link, typo, or organization issue.
- Avoid committing private identifiers, account details, or any certificate metadata that is not already meant to be public.

## Pull Requests

- Keep each pull request scoped to one platform, institution, or cleanup theme.
- Summarize which sections of the index changed.
- Fill out the PR template.
- Ensure any relevant checks pass before merging.
- Do not commit secrets, credentials, or sensitive data.
- Call out any broken links that were removed or replaced.
