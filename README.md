# The Architecture of Secret Detention

A scroll-driven visual investigation into Bangladesh's network of secret detention
and torture sites (2009-2024), based on the findings of the Commission of Inquiry
on Enforced Disappearances. Produced for The Daily Star.

## Running it

This is a plain static site — no build step, no dependencies to install.

- **Locally:** serve the folder with any static server, e.g.
  ```bash
  npx serve .
  # or
  python3 -m http.server 8000
  ```
  Then open the printed URL. (Opening index.html directly via file:// mostly works,
  but a local server is recommended so map tiles and fonts load cleanly.)

## Deploying to Vercel

1. Push this folder to a GitHub repository.
2. In Vercel: **Add New -> Project** and import the repo.
3. Framework Preset: **Other**. Leave Build Command and Output Directory **empty**
   (there is no build — Vercel serves the files as-is).
4. Deploy. `index.html` is served at the root URL.

## Structure

```
index.html      The site (one page, scroll-driven)
support.js      Rendering runtime (required — keep next to index.html)
assets/         Images, sketches, and The Daily Star logo
vercel.json     Static-hosting config
```

## Runtime notes

The page loads a few libraries from public CDNs at runtime (Google Fonts, GSAP,
Lenis, Leaflet) and map tiles from OpenStreetMap. An internet connection is required
for these; no API keys are needed.

## Source

Report of the Commission of Inquiry on Enforced Disappearances, Bangladesh —
mandate covering 6 January 2009 to 5 August 2024.
