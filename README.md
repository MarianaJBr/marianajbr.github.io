# marianajbr.github.io

Mariana Jaber's personal academic site. Pure HTML/CSS/JS, no build step,
no framework.

Live at: **https://marianajbr.github.io**
Repo: **github.com/MarianaJBr/marianajbr.github.io**

## Structure

```
index.html                     ← homepage: bio, research overview, projects, contact
pairs/
  index.html                   ← PAIRS project page (team, objectives, method, publications)
  visuals/
    spine_cosmic_web.html      ← 3D Plotly cosmic-web visualization, linked from pairs/index.html
```

The homepage is the front door — About, Research (a short overview, no
detailed bibliography), Projects, and Contact. Each project gets its own
folder; PAIRS is the first. As more projects start, add a new folder
(e.g. `next-project/index.html`) and a card for it in the homepage's
Projects section.

## Updating the live site

1. Go to `github.com/MarianaJBr/marianajbr.github.io` and open the file you
   want to change.
2. Click the **pencil icon** (top-right of the file view) to edit in the
   browser, or use **Add file → Upload files** to replace a file wholesale —
   GitHub will offer to overwrite when the filename and path match.
3. Commit the change.
4. Wait ~30–60 seconds, then refresh.

No "enable Pages" step is needed — that's already configured
(**Settings → Pages → Deploy from a branch → main → / (root)**).

## Editing

**Homepage (`index.html`)** sections and their anchors: `#about`,
`#research`, `#projects`, `#contact`. The Research section here is
intentionally a short overview with no publication list — the full
bibliography lives on the PAIRS page (linked from there).

**PAIRS page (`pairs/index.html`)** sections and anchors: `#about`, `#team`,
`#objectives`, `#method`, `#research` (full publication list), `#funding`.
Its nav and footer link back to the homepage's `#about` and `#contact`
sections rather than out to the old Wix site.

## Visuals

`pairs/visuals/spine_cosmic_web.html` is a self-contained Plotly export
(~2.2 MB — it bundles its own data, no extra files needed), live at
`https://marianajbr.github.io/pairs/visuals/spine_cosmic_web.html`.

Note: raw Plotly HTML exports often need a small CSS fix to actually
display — the exported wrapper `<div>` has no explicit height, and the plot
div is set to `height:100%`, which resolves to zero unless `html`/`body`/the
wrapper are given an explicit height first. This file already has that fix
applied. If you export a fresh Plotly HTML file later, add this to its
`<head>` before uploading it:

```html
<style>
  html, body { height: 100%; margin: 0; background: #0a0a0a; }
  body > div { height: 100vh; width: 100%; }
</style>
```

## CV

The nav and footer currently link out to the CV page on the old Wix site
(`jabermariana.wixsite.com/cosmology/cv`). Swap that link for a hosted PDF
or a dedicated `/cv/` page whenever you're ready to move it over.
