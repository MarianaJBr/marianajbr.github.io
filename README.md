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
   `index.html` (and `README.md` if you like) from this folder. Commit
   directly to the `main` branch.
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
