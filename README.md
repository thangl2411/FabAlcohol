# FabAlcohol offline website package

This package contains a complete static copy of the FabAlcohol website. It does not require Node.js, a database, a build command, or an internet connection for its layout, images, fonts, language switcher, FAQ, and product-story modals.

## Open the website

1. Extract the ZIP file to a normal folder.
2. Double-click `OPEN-WEBSITE.bat`, or open `index.html` directly in Chrome, Edge, Firefox, or Safari.
3. Keep `index.html` and the `assets` folder together. All image and font paths are relative to that structure.

## Rebuild or edit

The entire website is contained in `index.html`:

- HTML: page structure and visible content.
- CSS: colours, typography, responsive layout, cards, modal, and animation.
- JavaScript: VI/EN toggle, FAQ accordion, product-story modal, navigation, and Zalo placeholder behaviour.
- Images and fonts: stored under `assets/`.

Edit the file with any text/code editor, save, and refresh the browser. No compilation is required.

## Connect the real Zalo account

The exported design intentionally contains no invented phone number. Search `index.html` for `id="zaloCta"` and for `pendingZalo`. Replace the placeholder behaviour with your official Zalo URL, for example:

```html
<a class="btn" href="YOUR_OFFICIAL_ZALO_URL" id="zaloCta" target="_blank" rel="noopener">Liên hệ qua Zalo</a>
```

Then remove or replace the JavaScript listeners that call `pendingZalo`. Use only the verified official FabAlcohol account URL.

## Publish elsewhere

Upload the contents of this folder—not the outer folder itself—to any static host such as GitHub Pages, Netlify, Cloudflare Pages, an ordinary web server, or shared hosting. The host should serve `index.html` as the default page.

## Package map

```text
FabAlcohol-offline-package-2026-10-24/
├── index.html
├── OPEN-WEBSITE.bat
├── README.md
├── SITE-SPECIFICATION.md
├── RESOURCE-MANIFEST.md
└── assets/
    ├── hero.png
    ├── editorial.png
    ├── fonts/
    └── products/
```

## Important commercial-use note

Product facts and editorial sources are listed in `RESOURCE-MANIFEST.md`. Before a public commercial launch, confirm image licensing, current product specifications, prices, availability, delivery rules, and the official Zalo link.

