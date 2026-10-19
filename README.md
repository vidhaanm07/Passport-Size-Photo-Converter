# Passport Photo Maker

A fast, private passport photo tool. Upload any photo, pick a country's size, frame your face, and download a print-ready JPG/PNG or a tiled print sheet.

**Everything runs in the browser.** Photos are never uploaded, so the app needs no backend and scales to any number of users on a static host.

## Features

- Drag and drop, file picker, or paste from the clipboard
- Any format the browser can decode (JPG, PNG, WebP, GIF, BMP, AVIF, SVG; HEIC in Safari)
- Presets for UK/EU/Australia/Japan, USA/India, Canada, China, Schengen visa, ID card, plus a custom size
- Drag, scroll-zoom, and keyboard nudging with a face guide overlay
- Brightness, contrast, and background fill
- Export at 150, 300, or 600 dpi
- Print sheets for 4x6 in, 5x7 in, A4, and US Letter
- Futuristic animated UI (respects `prefers-reduced-motion`)

## Project structure

```
index.html     The whole app (HTML, CSS, JS in one file)
vercel.json    Vercel config: clean URLs, security headers, caching
package.json   Optional, provides `npm run dev`
LICENSE        VIDHAAN MATHUR
```

## Run locally

```bash
npm run dev          # serves on http://localhost:3000
# or simply open index.html in a browser
```

## Deploy

### GitHub

```bash
git init
git add .
git commit -m "Initial commit: passport photo maker"
git branch -M main
git remote add origin https://github.com/<your-username>/passport-photo-maker.git
git push -u origin main
```

### Vercel (dashboard)

1. Go to https://vercel.com/new and import the GitHub repo.
2. Framework Preset: **Other**. Leave Build Command and Output Directory empty.
3. Click **Deploy**. Every push to `main` redeploys automatically.

### Vercel (CLI)

```bash
npm i -g vercel
vercel          # preview deploy
vercel --prod   # production deploy
```

## Add a new country or size

Edit the `PRESETS` array at the top of the script in `index.html`. Sizes are in millimetres:

```js
{ id: 'br', label: 'Brazil — 50 × 70 mm', w: 50, h: 70 }
```

## Notes

- Fonts load from Google Fonts. The page falls back to system fonts if blocked.
- Always check the current photo rules of the issuing authority before submitting (head size, background, expression).

## License

VIDHAAN MATHUR
