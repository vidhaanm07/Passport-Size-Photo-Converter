<div align="center">

# Passport Size Photo Converter

**Turn any photo into a print-ready passport photo in seconds. Right in your browser.**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Deployed on Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-000000?logo=vercel&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![No backend](https://img.shields.io/badge/Backend-none-00e5ff)

[Live demo](https://YOUR-VERCEL-URL.vercel.app) · [Report a bug](https://github.com/vidhaanm07/Passport-Size-Photo-Converter/issues) · [Request a feature](https://github.com/vidhaanm07/Passport-Size-Photo-Converter/issues)

</div>

---

## Why this exists

Getting a passport or visa photo usually means a trip to a studio, or uploading a personal photo to a random website. This tool does the whole job on your own device. Your photo is processed in the browser using the Canvas API and is **never uploaded anywhere**.

Because there is no server to run, it is free to host and scales to any number of users.

## Features

- **Any image, any format.** Drag and drop, pick a file, or paste from the clipboard. It supports JPG, PNG, WebP, GIF, BMP, AVIF and SVG (and HEIC in Safari).
- **Country presets.** UK/EU/Australia/Japan (35 × 45 mm), USA and India (2 × 2 in), Canada (50 × 70 mm), China (33 × 48 mm), Schengen visa, ID card, plus a fully custom size.
- **Precise framing.** Drag to position, scroll or slide to zoom, and use the arrow keys to nudge. A face guide overlay shows where your head and eyes should sit.
- **Photo adjustments.** Brightness, contrast and a background fill colour (white, light grey, light blue or any custom colour).
- **Print-ready export.** Download JPG or PNG at 150, 300 or 600 dpi, at the exact pixel size for your chosen dimensions.
- **Print sheets.** Tile multiple copies on 4 × 6 in, 5 × 7 in, A4 or US Letter with cut lines.
- **Futuristic UI.** An animated neon grid, a glitch title, a scanning effect and a camera-flash on export. It respects `prefers-reduced-motion`.

## How to use it

1. Open the app and drop in a photo.
2. Choose the photo size for your country.
3. Drag and zoom until your face fits the guide.
4. Adjust brightness, contrast or the background if needed.
5. Download the single photo, or generate a print sheet.

## Tech stack

| Layer | Choice |
|---|---|
| Markup, styling, logic | Plain HTML, CSS and JavaScript in a single `index.html` |
| Image processing | HTML5 Canvas API (client-side) |
| Fonts | Orbitron and Share Tech Mono (Google Fonts, with system fallbacks) |
| Hosting | Vercel (static site, no build step) |

## Project structure

```
Passport-Size-Photo-Converter/
├── index.html     # the whole app
├── vercel.json    # clean URLs, security headers, caching
├── package.json   # provides `npm run dev`
├── README.md
├── LICENSE
└── .gitignore
```

## Run locally

```bash
git clone https://github.com/vidhaanm07/Passport-Size-Photo-Converter.git
cd Passport-Size-Photo-Converter
npm run dev        # serves at http://localhost:3000
```

You can also open `index.html` directly in a browser.

## Deploy your own

1. Fork this repo.
2. Go to [vercel.com/new](https://vercel.com/new) and import your fork.
3. Set the Framework Preset to **Other** and leave the build settings empty.
4. Click **Deploy**.

## Add a new country or size

Open `index.html` and add one line to the `PRESETS` array at the top of the script. Sizes are in millimetres:

```js
{ id: 'br', label: 'Brazil — 50 × 70 mm', w: 50, h: 70 }
```

## Roadmap

- [ ] Automatic face detection and centring
- [ ] One-click background removal
- [ ] Checks against each country's rules (head size, margins)
- [ ] More countries and visa types
- [ ] Installable PWA with offline support

Ideas and pull requests are welcome.

## Privacy

All processing happens locally in your browser. No images, files or personal data are sent to a server, stored or tracked.

## Disclaimer

Photo requirements change. Always check the current rules of the issuing authority (head size, background, expression, glasses) before you submit a photo.

## Contributing

1. Fork the project
2. Create a branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -m "Add my feature"`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a pull request

## License

Released under the [MIT License](LICENSE).

## Author

**Vidhaan Mathur**

- GitHub: [@vidhaanm07](https://github.com/vidhaanm07)
- Portfolio: [vidhaanmportfolio.vercel.app](https://vidhaanmportfolio.vercel.app/)

If this project helped you, consider giving it a star.
