# Hero images

Drop these two files in this folder:

- `hero-desktop.webp` — 16:9, ~2560×1440 (used by `index.html`)
- `hero-mobile.webp` — 9:16, ~1170×2532 (used by `index.html`)
- `about.webp` — 9:16 portrait from Midjourney (used by `about.html`)

Served by `<picture>` / `<img>` tags in the HTML. Mobile breakpoint is 768px.
The about page treats `about.webp` as a portrait card on desktop (no cropping)
and full-width on mobile.

## Re-encoding from PNG sources

PNG masters are kept locally (gitignored). To re-encode after replacing a master:

```sh
cwebp -q 85 hero-desktop.png -o hero-desktop.webp
```

Quality 85 is a good editorial sweet spot. Bump to 90 if you see artifacts in
smooth gradient areas; drop to 80 for smaller files when payload matters more.
