# Micaela Creo — Portfolio Site

A static, single-page portfolio (HTML/CSS/JS, no build step) styled to match the Notion palette. No upload limits here — add as many images as you like to `assets/`.

## What's built vs. placeholder

**Built:** Hero/About Me, Video block (placeholder video, real layout), Education Highlights (degrees, honors, press), Analytical Projects → Research Assistantship case study (full context/role/outcome, image placeholders).

**Placeholder (marked "Coming soon" / "In progress" on the site):** NY Excelsior Scholarship project, iHeartMedia project, full Resume section, full Skills & Contact section. Your resume is still linked live via Google Drive in the hero and Resume section.

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

## Adding your images

Drop files into `assets/`:
- `headshot.jpg` — your photo
- `research_1.png`, `research_2.png` — your two research screenshots

Then in `index.html`, replace the placeholder `<div class="placeholder-box ...">` / `<div class="img-placeholder">` blocks with `<img>` tags pointing to those files (a one-line swap — comments in the HTML mark exactly where).
