# Conventions & Schema (public docs)

Keep these consistent so URLs stay clean and pages render themed.

> This repo holds **public methodology** docs. Private per-band operational data
> (channel settings, device IPs, session templates) lives in the site's private
> `src/internal/` tier, which has its own schema — not here.

## Naming

- **Slugs** are lowercase, hyphenated, ASCII: `scenes-band-config`, `how-it-works`.
- One concept per file. A device's behaviour goes under `gear/<device>/`.
- Folder path = URL. `gear/m32/scenes-band-config.md` → `/docs/gear/m32/scenes-band-config/`.

## Frontmatter

Every doc starts with YAML frontmatter. `title` and `description` are required
(they drive the page hero, the `<title>`, and the docs index card).

```yaml
---
title: M32-Edit Scenes for band configurations
description: One-line summary used on the docs index and in the page meta.
tags: [scenes, workflow]   # optional topic tags
status: confirmed          # confirmed | draft | needs-testing
updated: 2026-10-20
---
```

The directory data file `docs.json` already applies `layout: docs.njk` and adds
every page to the `docs` collection, so individual files don't set those.

## Linking

Use absolute site paths between docs: `/docs/gear/m32/scenes-band-config/`.
