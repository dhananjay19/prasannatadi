# prasannatadi.com

Personal website for Dr. Prasanna Tadi, MD — hosted as a static site on GitHub Pages.

## Files

- `index.html` — the entire site (single page, self-contained HTML/CSS/JS, no build step)
- `CNAME` — tells GitHub Pages to serve this repo at `prasannatadi.com` (required — do not delete)

## Deploying (GitHub Pages)

1. Push these files to the `main` branch of this repo.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. Under **Custom domain**, confirm it shows `prasannatadi.com` (it should auto-fill from the CNAME file) and click **Save**.
5. At your domain registrar, set DNS:
   - Four **A** records for the apex domain (`prasannatadi.com`) pointing to:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - One **CNAME** record for `www` pointing to `dhananjay19.github.io`
6. Wait for DNS to propagate (usually under an hour), then check **Enforce HTTPS** in the Pages settings once GitHub shows the DNS check as successful.

## Editing the site

Everything — copy, styling, and layout — lives in `index.html`. Open it in any text editor. No dependencies to install, no build process; just edit and push.

To swap in a real headshot, replace the placeholder `<div class="hero-photo">...</div>` block with an `<img src="your-photo.jpg" alt="Dr. Prasanna Tadi">` and upload the image file to the repo alongside `index.html`.
