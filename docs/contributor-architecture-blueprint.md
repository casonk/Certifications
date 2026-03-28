# Contributor Architecture Blueprint

This document is the concise implementation map for `Certifications`. The repo's
real architecture is a curated documentation workflow: keep the root README as
the canonical catalog, store local certificate evidence under provider buckets,
and preserve provider-specific drilldown indexes where they help navigation.

## Canonical Catalog Surface

- `README.md` is the single source of truth for the public certification index.
- The root document groups the portfolio by platform and then by institution,
  module type, or recognition type where that makes navigation clearer.
- Each entry should preserve the same core contract:
  - course or platform page
  - public shareable completion or achievement link

## Evidence Archive Layer

1. `Coursera/`
   - Institution subdirectories hold the local PDF exports.
   - `Coursera/README.md` is the provider-level drilldown index.
2. `Microsoft/`
   - Splits local evidence into `Learning_Paths/` and `Modules/`.
   - `Microsoft/README.md` presents the provider-level summary.
3. `TryHackMe/`
   - Combines room lists, local badge images, a profile badge image, and local
     certificate PDFs under a single provider bucket.
4. `Recognitions/`, `Weber_State/`, and `LinkedIn/`
   - Hold simpler one-off evidence artifacts that do not need deeper internal
     taxonomies.

## Provider Drilldown Surface

- `Coursera/README.md`
- `Microsoft/README.md`
- `TryHackMe/README.md`
- `Recognitions/README.md`
- `Weber_State/README.md`

These provider readmes are secondary navigation aids. They may mirror or expand
platform-specific slices of the archive, but they should not supersede the
root README as the canonical portfolio index.

## Local Versus External Proof

- Local PDFs and images are the archived evidence artifacts tracked in git.
- External course pages and public share links are the public verification
  surfaces referenced from the indexes.
- Keep those two surfaces distinct in the architecture: the repo stores the
  archive, while the markdown indexes curate the outward-facing proof links.

## Contributor Workflow

1. Add the new artifact file under the correct provider bucket.
2. Update the nearest provider README when that drilldown surface exists.
3. Update the root `README.md` in the same change.
4. Keep naming, grouping, and live-link formatting consistent with the existing
   archive.

## Validation Surface

- `.github/workflows/ci.yml`
- `docs/diagrams/repo-architecture.puml`
- `docs/diagrams/repo-architecture.drawio`

The current CI is intentionally light because this is a documentation archive.
The main quality gate is structural consistency between the archive folders and
the curated indexes.

## Regeneration

```bash
cd ../../util-repos/archility
PYTHONDONTWRITEBYTECODE=1 PYTHONPATH=src python3 -m archility render ../../doc-repos/Certifications
```

## Contributor Notes

- Treat this file and the paired `docs/diagrams/` sources as the architecture
  handoff surface for the curation workflow.
- Update the blueprint and diagram sources together when provider buckets,
  provider drilldown files, or catalog conventions change.
