# cs-software-org.github.io

CS Software website — static HTML served by GitHub Pages at https://cs-software-org.github.io/.

## Structure

- `index.html` — home
- `touch-roulette/index.html` — Touch Roulette app page
- `privacy.html` — privacy policy (keep this URL; app store listings link to it)
- `404.html` — not-found page
- `assets/site.css` — shared styles (brand tokens at the top)
- `assets/` — app images and social share images (`assets/og/`)
- `brand/` — the logo kit (see below)
- `images/` — legacy logo paths kept working (`cs_software_logo.svg`/`.png` show the current logo)
- `robots.txt`, `sitemap.xml`, `llms.txt`, `site.webmanifest` — search and AI crawler files

## Brand

- Logo: an extended geometric "CS" with "SOFTWARE" in tracked DM Sans capitals. Use Ink on light backgrounds and Bone on dark ones.
- Colours: Ink `#1C2436`, Bone `#F4F1EA`, Paper `#FAFAF9`, Night `#111214`, and Touch `#E1603A` (the site's only accent, used for small details like headline full stops, never in the logo)
- Type: DM Sans (Google Fonts)

### Logo kit (`brand/`)

| Folder | What's in it |
| --- | --- |
| `logo/svg`, `logo/png`, `logo/pdf` | Stacked logo (primary), horizontal logo (`-horizontal`), and monogram (`cs-software-monogram`) in `ink`, `bone`, `black`, and `white`. PNGs are transparent, 1200 and 2400 px wide. PDFs are vector, for print. |
| `icons` | App icon (1024, 512, 192), `apple-touch-icon.png` (180), `favicon.svg`, `favicon.ico` (16/32/48) |
| `social` | Profile pictures (`avatar-dark`, `avatar-light`, 1024 px, safe for circle crops), X header (1500×500), LinkedIn banner (1128×191), email signature (600 px wide) |
| `store` | Google Play developer page icon (512×512) and header image (4096×2304) |

The site's `/favicon.svg`, `/favicon.ico`, and `/apple-touch-icon.png` are copies of the files in `brand/icons`; the header and footer inline the horizontal logo as SVG.

## Adding an app

1. Add an app page at `<app-name>/index.html`, using `touch-roulette/index.html` as a template (update its JSON-LD).
2. Add the app to the "Our apps" section and the FAQ on `index.html`.
3. Add the page to `sitemap.xml` and `llms.txt`.

## Search Console note

Google's "Software apps" report flags the Touch Roulette page for a missing `aggregateRating` or `review`. That's expected: the page deliberately doesn't mark up the store rating. The rest of the structured data (Organization, WebSite, BreadcrumbList, FAQPage) is unaffected.

## Preview locally

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000/. Pages use root-relative paths, so opening the files directly won't load styles.
