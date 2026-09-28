# cs-software-org.github.io

CS Software website — static HTML served by GitHub Pages at https://cs-software-org.github.io/.

## Structure

- `index.html` — home
- `touch-roulette/index.html` — Touch Roulette app page
- `privacy.html` — privacy policy (keep this URL; app store listings link to it)
- `404.html` — not-found page
- `assets/site.css` — shared styles (brand tokens at the top)
- `assets/` — app images, icons, and social share images (`assets/og/`)
- `images/` — logo files (`cs_software_logo.svg`, `cs_software_logo-dark.svg`, `cs_software_mark.svg`)
- `robots.txt`, `sitemap.xml`, `llms.txt`, `site.webmanifest` — search and AI crawler files

## Brand

- Colours: Ink `#1C2436`, Touch `#E1603A` (the only accent), Bone `#F4F1EA`, Paper `#FAFAF9`, Night `#111214`
- Type: DM Sans (Google Fonts)

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
