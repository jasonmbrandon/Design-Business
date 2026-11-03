# Design Business — landing page

The one-page landing page for the business vision document: a downloadable PDF
(plus the editable Word version) presented with its own preview.

## What's here

| File | What it is |
|---|---|
| `index.html` | The landing page. One self-contained file — no build step, no dependencies, no external fonts or CDNs. |
| `business-vision-and-personal-goals.pdf` | The document itself. Letter size, one page, 33 KB. |
| `business-vision-and-personal-goals.docx` | The editable Word version, for when a number changes. |
| `preview.png` | Page one rendered at 2× (1224 × 1584) for the sheet image on the page. |

## Viewing it locally

Open `index.html` directly, or serve the folder so the download buttons behave
exactly as they will online:

```bash
python -m http.server 8000
# then open http://127.0.0.1:8000
```

## Publishing with GitHub Pages

Settings → Pages → Source: *Deploy from a branch* → branch `main`, folder `/ (root)`.
The page is already root-relative and `.nojekyll` is present, so it serves as-is at
`https://jasonmbrandon.github.io/Design-Business/`.

## Updating

The document is the source of truth; the page summarises it. If a number changes,
rebuild the PDF and Word file, regenerate `preview.png`, then update the matching
line in `index.html` so the two never disagree.
