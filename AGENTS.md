# AGENTS.md

## Project Purpose

Personal certification portfolio documenting completed courses and certifications from Coursera, Microsoft, LinkedIn, TryHackMe, Weber State, and other learning platforms. This is a documentation-only repo with no code.

## Repository Layout

- `Coursera/` — Coursera course certificates (subdirs per university/course)
- `Microsoft/` — Microsoft certifications
- `LinkedIn/` — LinkedIn Learning certificates
- `TryHackMe/` — TryHackMe cybersecurity path certificates
- `Weber_State/` — Weber State University credentials
- `Recognitions/` — Awards and recognitions
- `README.md` — Master index of all certifications with links

## Operating Rules

- Keep the README as the single source of truth for the certification index.
- When adding a new certification, add both the file and its README entry in the same commit.
- Use descriptive commit messages: `docs: add <Platform> - <Course Name>`.
- Organize certificates into platform-specific subdirectories.
- Prefer PDF or image formats for certificate files.
- Do not commit personal information beyond what is already publicly visible on the certificate.

## Content Guidelines

- Each certification entry in README should include:
  - Course name with link to the course page
  - Live link to the shareable certificate
- Group entries by platform, then by institution where applicable.

## Agent Memory

Use `./CHATHISTORY.md` as the standard local handoff file for this repo.

- It is local-only and gitignored.
- Read it after `AGENTS.md` when resuming work.
- Keep entries brief: objective, key actions, blockers, and next step.
- Redact private or account-specific data before writing to it.
