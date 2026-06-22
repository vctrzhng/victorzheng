# Personal site

A warm, minimal personal website. Plain HTML and CSS — no build step, no
framework, nothing to install. Just edit the files and push.

## Files

- `index.html` — the page content. Look for `EDIT ME` comments; that's where
  your words, links, and projects go.
- `styles.css` — the look. All the colors, fonts, and spacing live as
  variables at the very top under `:root`. Change one value there and it
  updates everywhere.
- `favicon.png` — *(add your own)* the little icon in the browser tab, 32×32 or
  larger.
- `images/` — *(add this folder)* where your travel photos go.

## Preview it on your computer

Just double-click `index.html` to open it in a browser. That's it.

If links or fonts act up, run a tiny local server from this folder instead:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Make it yours

1. Open `index.html` and replace everything marked `EDIT ME` — your intro, your
   social links (change the `#` and `you@example.com` to real ones), your
   projects and work.
2. To change the vibe, open `styles.css` and edit the tokens at the top.
   - Want a different accent than terracotta? Change `--accent`.
   - Want it less cream? Change `--bg`.
   - Different heading font? Swap the Google Fonts link in `index.html` and
     update `--font-display`.
3. Add travel photos: make an `images/` folder, drop photos in, and in the
   Travel section swap each `<div class="ph ...">` for
   `<img src="images/yourphoto.jpg" alt="Short description" />`. Portrait
   (4:5) crops look best.

## Put it on GitHub Pages (free hosting)

**The quick way (GitHub website):**

1. Create a new repository on GitHub.
   - Name it `personal-site` for a URL like
     `https://YOURNAME.github.io/personal-site/`, **or**
   - Name it exactly `YOURNAME.github.io` to get the clean root URL
     `https://YOURNAME.github.io/`.
2. Upload these files (drag them into the repo's "Add file → Upload files").
3. Go to **Settings → Pages**, set **Source** to *Deploy from a branch*, pick
   `main` and `/ (root)`, and save.
4. Wait about a minute, then refresh. Your site is live.

**The command-line way:**

```bash
git init
git add .
git commit -m "Initial personal site"
git branch -M main
git remote add origin https://github.com/YOURNAME/REPO.git
git push -u origin main
```

Then do step 3 above to turn on Pages.

## A custom domain (optional)

To get a clean link like `victorzheng.com` instead of the `github.io` URL:

1. Buy a domain (~$10–15/yr at Cloudflare, Namecheap, Porkbun, etc.).
2. In **Settings → Pages → Custom domain**, enter your domain.
3. At your registrar's DNS settings, add a `CNAME` record pointing your domain
   (or a subdomain like `www`) to `YOURNAME.github.io`.
4. Back in Pages settings, check **Enforce HTTPS**.

## Before you share it

- Drop in a `favicon.png`.
- Make an `og.png` (a nice 1200×630 image) and update the `og:image` and
  `og:url` lines in `index.html` — that's the preview card people see when you
  share the link.
