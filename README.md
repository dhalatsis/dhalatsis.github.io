# dhalatsis.github.io

Personal website. Plain HTML and CSS — no build step, no dependencies, no framework.

## Files

```
index.html    the entire site
style.css     all styling (light/dark via prefers-color-scheme)
assets/       avatar.jpg, cv.pdf
.nojekyll     tells GitHub Pages to serve files as-is
```

## Editing

Open `index.html` and edit the text. That's it. Common changes:

- **Add a publication** — copy an existing `<div class="pub">` block, change the fields.
  `<span class="me">` marks your own name in the author list.
- **Change the status pill** — the `<div class="status">` line in the header.
- **Update the CV** — replace `assets/cv.pdf`.
- **Colours** — the `:root` block at the top of `style.css`; the dark palette is
  the `@media (prefers-color-scheme: dark)` block directly below it.

## Preview locally

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Deploy

Push to `main`. GitHub Pages serves the repo root — no Actions workflow, no build.

Settings → Pages → Source: *Deploy from a branch* → `main` / `/ (root)`.
