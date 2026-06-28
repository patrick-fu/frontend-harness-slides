# Frontend Harness Slides

**[中文说明](README.zh-CN.md)**

`frontend-harness-slides` builds a slide deck as a real engineering project — a Playwright **harness** guards every frame, a **registry** decouples slide order from filenames, and an absolute 16:9 **stage** keeps the layout identical on any screen. It is a step up from single-file HTML slides: robust, maintainable, and hard to break as the deck grows or gets edited across many sessions.

## Install

```bash
npx skills add patrick-fu/frontend-harness-slides
```

Update later:

```bash
npx skills update
```

## What It Does

- **Registry, not filenames** — one central array owns slide order, so inserting a slide never renames files or breaks snapshots ("re-indexing hell").
- **Absolute 16:9 stage** — content lives on a virtual 1920×1080 canvas scaled as a whole; no per-device reflow.
- **A real test harness** — Playwright freezes animations into a stable frame, pixel-compares every scene and beat, and audits layout (a 16px font floor, nothing escaping the stage). A change is done only when the harness is green.
- **Built to last** — query-routed state (`?scene=&beat=`), theme discovery by eye, PDF export, and a query-safe Vercel deploy, all wired for long-term iteration.

## When To Use It

Reach for it when you want a presentation that stays solid as it grows — created, extended, or refactored over time — rather than a quick one-off single-file deck.

## More Skills

For more reusable agent skills, see
[Awesome Skills](https://github.com/patrick-fu/awesome-skills).
