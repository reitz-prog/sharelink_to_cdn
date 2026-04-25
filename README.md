# Google Drive to Shareable Image

A static, client-side tool that converts Google Drive share links into direct `lh3.googleusercontent.com` CDN URLs at multiple sizes.

**Live:** https://reitz-prog.github.io/sharelink_to_cdn/

## Features

- **Single link** — paste a Drive URL, get CDN links instantly
- **Bulk paste** — drop in any text; Drive IDs are auto-extracted
- **File upload** — `.txt`, `.csv`, `.html`, `.md`, `.json` (any text format)
- **5 size presets** — Thumbnail, Small, Medium, Large, Original (toggleable)
- **Live thumbnails**, per-row copy, **Copy all (CSV)**, **Download CSV**
- 100% client-side — no backend, no tracking

## Supported input formats

The extractor recognizes Drive IDs from:

- `https://drive.google.com/file/d/FILE_ID/view`
- `https://drive.google.com/open?id=FILE_ID`
- `https://drive.google.com/uc?id=FILE_ID`
- Existing `https://lh3.googleusercontent.com/d/FILE_ID=...` URLs
- Bare file IDs (one per line)

## Output format

```
https://lh3.googleusercontent.com/d/FILE_ID=s800
```

Where the suffix controls size: `s200`, `s400`, `s800`, `s1600`, `s0` (original).

## Requirements

The Drive file must be **shared publicly** ("Anyone with the link can view") for the CDN URL to load.

## Local development

It's a single `index.html` — open it in any browser:

```bash
xdg-open index.html
```

## Deploying your own copy

1. Fork this repo
2. **Settings → Pages → Source: Deploy from a branch → `main` / `(root)` → Save**
3. Visit `https://<your-username>.github.io/sharelink_to_cdn/`
