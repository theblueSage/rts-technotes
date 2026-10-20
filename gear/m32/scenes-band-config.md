---
title: M32-Edit Scenes for band configurations
description: Each band configuration is saved as its own M32 Scene — what a Scene stores and the gotchas.
tags: [scenes, shows, snippets, workflow]
status: confirmed
updated: 2026-10-19
---

**Confirmed:** Using M32-Edit, each band configuration is saved as its own
**Scene**. This is the intended workflow — a Scene is a full snapshot of the
console state.

## What a Scene stores

- Channel configs (names, colors, input source/routing)
- Preamp (head amp) gain, phantom power (+48V), polarity
- EQ, dynamics (gate/comp), inserts
- Fader levels, mutes, pan
- Bus/aux sends and routing, FX rack settings

## Structure

- Scenes live inside a **Show** (the container, up to 100 Scenes). One Show file
  holds all band Scenes — one Scene per band.
- **Snippets** = *partial* recalls (only selected parameters/channels) when you
  want to change part of the desk without recalling everything.
- M32-Edit can build and save Shows/Scenes **offline**, then sync to the console.

## Caveats

- **Preamp gain is stored in the Scene** — recalling a band's Scene resets
  head-amp gain. Fine for a single console.
- If sharing a stagebox / AES50 split with another console (e.g. a monitor desk),
  gain changes propagate to both desks. Coordinate, or use gain tracking.
- **Scene Safes / Channel Safes** exclude chosen parameters or channels from
  recall (e.g. keep gains steady across band changes).
