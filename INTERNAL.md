# hatchlabs-web internal notes

Static site for Hatch Labs, published via GitHub Pages.

## Current status

- Public site: Hatch Labs and Hidey
- Hidey public pages now exist in Japanese and English under `docs/`
- Draft copies are still kept under `drafts/` for editing
- Hidey English support includes dedicated English legal pages
- GitHub Pages publish source: `main` branch / `docs` folder
- Custom domain: `hatchlaboratories.com`
- Public contact address: `contact@hatchlaboratories.com`
- Hidey draft contact address: `hidey@hatchlaboratories.com`

## Page structure

Public pages in `docs/`

- `/docs/index.html`
  - Hatch Labs top page
  - Sections: `About`, `Apps`, `Contact`
  - Links to the public Hidey page from the `Apps` section
- `/docs/hidey/index.html`
  - Public Hidey landing page in Japanese
- `/docs/en/hidey/index.html`
  - Public Hidey landing page in English
- `/docs/privacy/index.html`
  - Privacy policy
- `/docs/legal/index.html`
  - Legal notice / 特定商取引法に基づく表記
- `/docs/en/privacy/index.html`
  - English privacy policy
- `/docs/en/legal/index.html`
  - English legal notice
- `/docs/styles.css`
  - Shared public styles for the Hatch Labs and Hidey pages
- `/docs/assets/Hidey-5.png`
  - Hidey logo used in the public `Apps` card
- `/docs/assets/Hidey.svg`
- `/docs/assets/hidey-before.PNG`
- `/docs/assets/hidey-after.PNG`
- `/docs/assets/hidey-before-en.PNG`
- `/docs/assets/hidey-after-en.png`
- `/docs/assets/before.PNG`
- `/docs/assets/after.JPG`
- `/docs/assets/before-en.PNG`
- `/docs/assets/after-en.JPG`
  - Assets used by the public Hidey pages

Draft pages outside the publish path

- `/drafts/hidey/index.html`
  - Hidey product landing page draft in Japanese
  - Includes the interactive before/after slider, feature cards, and the draft contact UI
- `/drafts/en/hidey/index.html`
  - Hidey product landing page draft in English
  - Mirrors the public English page for ongoing edits
- `/drafts/en/privacy/index.html`
  - English privacy policy draft source
- `/drafts/en/legal/index.html`
  - English legal notice draft source

Local working copies kept outside `docs/`

- `/index.html`
- `/privacy/index.html`
- `/legal/index.html`
- `/styles.css`

These mirror the public site sources for local editing. Public deployment currently depends on the copied files in `docs/`.

## Design direction

- Hatch Labs top page:
  - Intentionally minimal
  - Quiet, restrained layout
  - Simple typography and low-contrast card treatment
- Hidey draft page:
  - Separate visual language from Hatch Labs
  - Softer, more playful product presentation
  - Uses real screenshots and an interactive before/after comparison in the hero
  - Includes a draft contact section with prefilled email templates and an X link

## Assets

- `/assets/Hidey.svg`
  - Current Hidey wordmark used in the Hidey draft page header
- `/assets/HideyTopTitle.pdf`
- `/assets/HideyTopTitle.png`
  - Hidey title assets kept for reference / alternate use
- `/assets/HideyEditTitle.pdf`
  - Alternate title asset kept for reference
- `/assets/hidey-before.png`
- `/assets/hidey-after.png`
  - Screenshots currently used in the Hidey draft hero slider
- `/assets/hidey-before-en.PNG`
- `/assets/hidey-after-en.png`
  - English-specific screenshots used in the Hidey English draft hero slider
- `/assets/before.png`
- `/assets/after.JPG`
  - Output/result images used in the Hidey draft preview section
- `/assets/before-en.PNG`
- `/assets/after-en.JPG`
  - English-specific preview images used in the Hidey English draft compare section
- `/private-assets/hidey/label-before.svg`
- `/private-assets/hidey/label-after.svg`
  - Private helper label assets for image editing; not referenced by the site

## Deployment

GitHub Pages

1. Push changes to `main`
2. GitHub Pages serves from `/docs`
3. Custom domain is configured as `hatchlaboratories.com`

Cloudflare

- DNS points the root domain to GitHub Pages using the four GitHub A records
- `www` is configured as a CNAME to `hatchlabs-app.github.io`
- DNS proxy should stay `DNS only` for the GitHub Pages records

## Publish checklist for current state

- Public pages are served from `docs/`
- Hidey public paths now exist in both Japanese and English
- Hero screenshots now assume the `Before` / `After` labels are baked into the image assets rather than rendered in HTML
- If editing drafts after this point, copy the final changes back into `docs/` before publishing

## Publish on GitHub Pages

1. Push changes to the default branch
2. In GitHub repository settings, enable Pages from the `main` branch and `/docs` folder
3. Confirm the custom domain remains set to `hatchlaboratories.com`

## Local preview

- Hatch Labs public site:
  - `http://127.0.0.1:8000/`
- Hidey draft (Japanese):
  - `http://127.0.0.1:8000/drafts/hidey/`
- Hidey draft (English):
  - `http://127.0.0.1:8000/drafts/en/hidey/`

If you want to preview locally, open `index.html` in a browser or run a simple static server.
