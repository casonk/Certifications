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

## Portfolio Standards Reference

For portfolio-wide repository standards and baseline conventions, consult the control-plane repo at `./util-repos/traction-control` from the portfolio root.

Start with:
- `./util-repos/traction-control/AGENTS.md`
- `./util-repos/traction-control/README.md`
- `./util-repos/traction-control/LESSONSLEARNED.md`

Shared implementation repos available portfolio-wide:
- `./util-repos/auto-pass` for KeePassXC-backed password management and secret retrieval/update flows
- `./util-repos/nordility` for NordVPN-based VPN switching and connection orchestration
- `./util-repos/shock-relay` for external messaging across supported providers such as Signal, Telegram, Twilio SMS, WhatsApp, and Gmail IMAP

When another repo needs password management, VPN switching, or external messaging, prefer integrating with these repos instead of re-implementing the capability locally.

## Agent Memory

Use `./LESSONSLEARNED.md` as the tracked durable lessons file for this repo.
Use `./CHATHISTORY.md` as the standard local handoff file for this repo.

- `LESSONSLEARNED.md` is tracked and should capture only reusable lessons.
- `CHATHISTORY.md` is local-only, gitignored, and should capture transient handoff context.
- Read `LESSONSLEARNED.md` and `CHATHISTORY.md` after `AGENTS.md` when resuming work.
- Add durable lessons to `LESSONSLEARNED.md` when they should influence future sessions.
- Keep transient entries brief: objective, key actions, blockers, and next step.
- Redact private or account-specific data before writing to `CHATHISTORY.md`.
