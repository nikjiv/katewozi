# katewozi.com

Personal site for Kate. Static — single HTML file, two images, one Google Fonts link. No build step.

## Files

- `index.html` — the hero page (`/`)
- `about.html` — the about page (`/about`)
- `vercel.json` — enables clean URLs (`/about` instead of `/about.html`)
- `images/hero-desktop.webp` — desktop hero (16:9, ~2560×1440) — **add this**
- `images/hero-mobile.webp` — mobile hero (9:16, ~1170×2532) — **add this**
- `images/about.webp` — about portrait (9:16) — **add this**
- `favicon.ico` — drop in the repo root when ready

## Local preview

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy to Vercel

1. Push the repo to GitHub.
2. In Vercel: **Add New → Project**, import the repo. No framework, no build command, no output directory — Vercel auto-detects static.
3. After the first deploy, go to **Project → Settings → Domains** and add `katewozi.com` and `www.katewozi.com`. Follow the DNS records Vercel shows for your registrar (typically an `A` record on the apex pointing to `76.76.21.21` and a `CNAME` on `www` pointing to `cname.vercel-dns.com`).
4. Vercel will issue the SSL cert automatically once DNS resolves.
