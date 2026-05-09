# Hero images

Drop these two files in this folder:

- `hero-desktop.webp` — 16:9, ~2560×1440 (used by `index.html`)
- `hero-mobile.webp` — 9:16, ~1170×2532 (used by `index.html`)
- `about.webp` — 9:16 portrait from Midjourney (used by `about.html`)

Served by `<picture>` / `<img>` tags in the HTML. Mobile breakpoint is 768px.
The about page treats `about.webp` as a portrait card on desktop (no cropping)
and full-width on mobile.
