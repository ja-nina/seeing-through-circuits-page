# Seeing Through Circuits — project page

Static GitHub Pages site for the paper
**"Seeing Through Circuits: Faithful Mechanistic Interpretability for Vision Transformers"**
(Żukowska, Stammer, Schiele, Fischer — ECCV 2026, arXiv:2604.14477).

## Files

| Path | Purpose |
|------|---------|
| `index.html` | The whole page — HTML + inline CSS + a tiny copy-to-clipboard script. No build step. |
| `images/method.png` | Figure 2, extracted from the manuscript (shown in "How Vi-CD works"). |
| `images/teaser.png` | Figure 1 — not shown on the page any more; kept only as the social-preview image (`og:image`). Safe to delete if you also remove the `og:image`/`twitter` meta tags. |
| `images/eccv2026.svg` | ECCV 2026 logo (from eccv.ecva.net); shown small, top-right, on a white chip so it stays legible in both themes. |
| `.nojekyll` | Tells GitHub Pages to serve the folder as-is (skip Jekyll). |

## Inspect it locally

**Quickest:** double-click `index.html` — it opens in your browser (`file://…`), images and all.

**Closer to the real thing** (serves over HTTP, like GitHub Pages will):

```powershell
cd C:\Users\ismyn\UNI\MPI\pages
python -m http.server 8000
```

then open <http://localhost:8000>. Stop the server with `Ctrl+C`.

**Checking the responsive / theme behaviour** in Chrome or Edge:

- Open DevTools (`F12`).
- Mobile layout: click the device-toolbar icon (`Ctrl+Shift+M`).
- Dark vs light: DevTools → `⋮` → *More tools* → *Rendering* → *Emulate CSS media feature `prefers-color-scheme`*.
  (Or just flip Windows to dark mode: Settings → Personalization → Colors.)

## Upload it to GitHub Pages

### Option A — command line

```powershell
cd C:\Users\ismyn\UNI\MPI\pages
git init
git add .
git commit -m "Project page for Seeing Through Circuits"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

Then on github.com: **repo → Settings → Pages → Build and deployment → Source: “Deploy from a branch” → Branch: `main` / folder `/ (root)` → Save.**
After ~1 minute the site is live at `https://<your-username>.github.io/<repo-name>/`.

> Tip: if you name the repo exactly `<your-username>.github.io`, it is served at
> `https://<your-username>.github.io/` (no sub-path).

### Option B — no command line

1. On github.com click **New repository**, make it **public**, create it.
2. On the empty repo page click **uploading an existing file**.
3. Drag in `index.html`, the `images` folder, `.nojekyll`, and `README.md`. Commit.
4. **Settings → Pages** → same as above.

## To do later

- **Code** button: uncomment the block in `index.html` (search `Code not released yet`) and set the URL.
- **Proceedings DOI**: once the ECCV 2026 / Springer LNCS DOI exists, add a DOI button and a `doi = {…}` line to the BibTeX.
- Add a video / demo section if there is one.
