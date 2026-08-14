# Micaela Creo — Portfolio Site

A static, single-page portfolio (HTML/CSS/JS, no build step, no framework) — free to host on GitHub Pages with no upload limits.

## What's on the site

- **Hero / About Me** — headshot, tagline, bio, and quick links (location, email, LinkedIn, resume)
- **Video intro** — link out to a short "get to know me" video
- **Education Highlights** — Wake Forest MSBA + BA, honors, awards, and press mentions (Phi Beta Kappa, GradTab feature)
- **Analytical Projects** (filterable by tag) —
  - *Research Assistantship*: data cleaning & visualization for a Wake Forest Economics research project on student mobility in Lima, Peru
  - *Difference-in-Differences Model*: senior econometrics project evaluating NY's Excelsior Scholarship
  - *Multiple Regression Model*: MSBA team project modeling Spotify track popularity in Excel & Python
- **Resume** — live embedded preview + download link (Google Drive)
- **Skills & Contact** — technical skills pulled from your resume, plus email/LinkedIn

Everything is built out — no placeholder or "coming soon" sections remain.

## Design notes

- **Fonts:** EB Garamond (headings), Literata (body) — loaded from Google Fonts
- **Palette:** gold (Wake Forest / education only), cream (page background), pink, sage, coral — defined as CSS variables at the top of `style.css` if you ever want to retheme
- **Interactions:** sticky nav with smooth scroll, scroll-reveal on sections, hover-grow on buttons/pills, hover-preview thumbnails on a few inline links, project filter pills

## Local preview

Just open `index.html` in a browser — no server needed.

## Deploy to GitHub Pages

1. Create a new repository on GitHub (e.g. `micaela-portfolio`).
2. Upload these files (`index.html`, `style.css`, `script.js`, `assets/`) to the repo — either drag-and-drop via the GitHub web UI ("Add file" → "Upload files") or via git:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to "Deploy from a branch", branch `main`, folder `/ (root)`.
5. Save. Your site will be live in a minute or two at `https://<your-username>.github.io/<repo-name>/`.

(Full beginner-friendly, no-command-line version of these steps is in `DEPLOY-GUIDE.md`.)

## Updating content later

Once live, edit any file directly in the GitHub web UI (pencil icon → edit → commit) and the site rebuilds automatically within a minute or two. See `DEPLOY-GUIDE.md` for the no-code walkthrough.

## About the `assets/` folder

Only the compressed images are actually referenced in `index.html` (mostly the `-sm` / `-table` files). A few original, uncompressed source images and PDF-render intermediates are still sitting in the folder from when they were built — you can delete these before your final upload to keep the repo lean, or just leave them (GitHub Pages won't serve anything that isn't linked from the HTML, so they're harmless either way):

- `headshot.jpg` (→ using `headshot-sm.jpg` instead)
- `research_1.png`, `research_2.png`, `research-poster.png` (→ using the `-sm.jpg` versions)
- `alba-vivar-sm.jpg` (unused — replaced by `alba-vivar-team-sm.jpg`)
- `did-page11-11.png`, `did-regression-crop.png` (intermediate crops → final is `did-regression-table.jpg`)
