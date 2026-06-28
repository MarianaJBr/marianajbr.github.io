# PAIRS — project site

A single-page site for the PAIRS cosmology project, built from the content on
the [PAIRS page](https://jabermariana.wixsite.com/cosmology/pairs) of Mariana
Jaber's site. Pure HTML/CSS/JS, no build step.

## Deploy to GitHub Pages (web UI, no terminal needed)

You're [MarianaJBr](https://github.com/MarianaJBr) on GitHub, so:

1. Go to [github.com/new](https://github.com/new) and create a repository —
   `pairs-site` works fine, or name it `marianajbr.github.io` if you want this
   to live at the root of your personal GitHub domain instead of a sub-path.
2. On the new repo's page, click **Add file → Upload files**, and drag in
   `index.html`, `README.md`, and the whole `visuals/` folder (containing
   `spine_cosmic_web.html`) from this folder. Commit directly to the `main`
   branch. GitHub's drag-and-drop upload preserves folder structure, so
   `visuals/spine_cosmic_web.html` will end up at the right path automatically.
3. Go to **Settings → Pages** (left sidebar).
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Under **Branch**, choose `main` and folder `/ (root)`, then **Save**.
6. Wait ~1 minute, then refresh — GitHub will show a green box with your live URL:
   - `https://marianajbr.github.io/pairs-site/` if you used that repo name, or
   - `https://marianajbr.github.io/` if you named the repo `marianajbr.github.io`.

## Deploy via git (command line)

```bash
git init
git add index.html README.md
git commit -m "PAIRS project site"
git branch -M main
git remote add origin https://github.com/MarianaJBr/pairs-site.git
git push -u origin main
```

Then enable Pages the same way as steps 3–5 above.

## Editing

Everything lives in `index.html` — content, styles, and the small amount of
JS for the mobile nav are all in that one file. Section anchors (`#team`,
`#objectives`, `#method`, `#scope`, `#funding`) match the nav links if you
want to add or reorder content.

## Visuals

`visuals/spine_cosmic_web.html` is a self-contained Plotly export (~2.2 MB —
it bundles its own data, so it works standalone with no extra files). It's
linked from the "Cosmic-web environment" objective card. To swap in a
different Plotly export, just replace that file and keep the same name, or
update the `href` in `index.html` if you rename it. Drop additional Plotly
HTML exports in the same `visuals/` folder and link to them the same way.
