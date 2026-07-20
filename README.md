# simmerandsear.com

Marketing + support site for **Simmer & Sear**, a recipe box for iPhone.
Static HTML/CSS, no build step, served by GitHub Pages at
[simmerandsear.com](https://simmerandsear.com).

## Pages

| URL | File | Purpose |
| --- | --- | --- |
| `/` | `index.html` | Landing page |
| `/help` | `help.html` | Help & support (App Store Support URL) |
| `/privacy` | `privacy.html` | Privacy policy (App Store Privacy URL) |
| 404 | `404.html` | Not-found page |

`styles.css` is the shared theme; tokens mirror the app's asset catalog
(accent `#CE4720` light / `#F2714D` dark, warm paper grounds, serif display).

## Assets

`assets/` holds favicons/touch icons derived from the app icon and
downscaled (720px-wide) App Store screenshots. Regenerate from the app repo
(`simmer-sear`) with `sips` if the icon or screenshots change.

## Local preview

```bash
python3 -m http.server 8000
# then open http://localhost:8000/index.html
```

Note: extensionless URLs (`/help`, `/privacy`) resolve on GitHub Pages but
not under `python -m http.server` — open the `.html` files directly for local
review.

## Deploy

Push to `main`; GitHub Pages (Settings → Pages → Deploy from branch → `main`
/ root) publishes automatically. `CNAME` binds the custom domain; `.nojekyll`
skips the Jekyll build.

**Status:** DNS on Cloudflare (unproxied) pointing at GitHub Pages; HTTPS cert provisioning in progress.
