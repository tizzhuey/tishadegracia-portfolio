# Portfolio Site

Static site (no build step) implementing the sitemap: Hero (with photo) → About → Construction & Project Coordination (5 projects) → CAD & 3D Modeling (16 projects) → Skills → Resume → Contact.

## Files
- `index.html` — the one-page site, with a photo card for every project
- `project-pm-01.html` … `project-pm-05.html` — one page per Construction & Project Coordination project
- `project-cad-01.html` … `project-cad-16.html` — one page per CAD/3D project
- `project-template.html` — the master template; only edit this if you want to change the *layout* of every project page at once
- `assets/` — put `profile.jpg`, `resume.pdf`, and all project images/drawings here

## Deploy to GitHub Pages
1. Push this folder to a GitHub repo.
2. Repo → **Settings → Pages** → Source: `main` branch, `/root`.
3. Your site publishes at `https://<username>.github.io/<repo>/`.

## Filling in each project
For each `project-pm-XX.html` / `project-cad-XX.html`:
1. Open the file, click the pencil (edit) icon.
2. Replace `[Project Name]`, location, role, overview, and involvement text.
3. Replace the `<div class="ph">Photo / drawing N</div>` lines in the gallery with `<img src="assets/your-photo.jpg" alt="...">` once you've uploaded that photo to `assets/`.
4. Commit.

Then in `index.html`, find that project's card and:
- Set its `<img class="card-img" src="assets/...">` to the thumbnail you uploaded.
- Fill in `[PROJECT TYPE — YEAR]` and `[Project Name N]`.

## Before adding real content
- [ ] Upload `assets/profile.jpg` and confirm it shows in the hero
- [ ] Add `assets/resume.pdf`
- [ ] Replace `you@example.com` and the LinkedIn placeholder
- [ ] Fill in and add photos to each of the 21 project pages (see above)
- [ ] Fill in each project card's thumbnail, type/year, and name in `index.html`
- [ ] Keep the "Project Scope (Team)" vs "My Contribution" split honest on each project page
- [ ] Contact form currently has no backend — wire it to Formspree, Netlify Forms, or similar, or leave it as `mailto:` only

## Notes
- Nav and structure follow the "simple navigation, few pages" recommendation — one main page, one repeatable project-detail page format used 21 times.
- Category 2 (CAD/3D) cards use a dashed border to visually separate technical-drafting work from full project-coordination work.
- Project card grid auto-wraps, so it stays tidy whether you have 5 or 16 items in a section.
