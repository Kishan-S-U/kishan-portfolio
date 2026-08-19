# Kishan Sanka Umesh — Portfolio

A static site — plain HTML, CSS, and JS, no build step. Ready to push straight to GitHub Pages.

## Deploy to GitHub Pages

1. Create a new repository on GitHub (e.g. `kishan-portfolio`).
2. Push this folder's contents to the repo root:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Your site will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

When you later buy a custom domain, add a `CNAME` file with your domain name at the repo root and point your domain's DNS to GitHub Pages — GitHub's docs walk through this under "Managing a custom domain."

## Before you publish — things I couldn't fill in for you

- [ ] **LinkedIn URL** — currently a placeholder (`linkedin.com/in/REPLACE-WITH-YOUR-LINKEDIN`) in `index.html` and every file in `projects/`. Find-and-replace across all files once you have the real link.
- [ ] **BE-level projects** — `projects/sensor-fusion-logger.html` and `projects/digital-control-simulator.html` are dummy placeholders (as requested) with a visible "Dummy content" banner. Replace the titles, copy, and tags with your real BE projects, and update their cards in `index.html`'s Projects section (`data-group="be"`).
- [ ] **Blog posts** — the Writing section is set up as a "coming soon" state. When you're ready to publish, the simplest path is a new `writing/post-slug.html` per post (copy a project page's structure), linked from the Writing section.
- [ ] **Photo (optional)** — you chose a monogram (`KSU`) over a photo for now. If you change your mind, the mark is defined in `css/style.css` under `.mark` / `.mark-lg` — swap it for an `<img>` if you'd like a real photo instead.

## Structure

```
index.html                 → single-page site: hero, about, experience, education, projects, writing, contact
projects/*.html             → one page per project, linked from the project cards
css/style.css                → all styling (design tokens at the top of the file)
js/script.js                → nav behaviour, scroll reveal, project filter tabs
favicon.svg                  → browser tab icon
```

## Notes on the design

Dark, matte PCB green with a muted copper accent — a deliberate nod to circuit boards rather than a generic dark theme. The hero's animated line is styled after an oscilloscope trace; the timeline markers in Experience and Education are drawn like solder pads on a trace line. Fonts: Instrument Sans for headings, Inter for body copy, IBM Plex Mono for dates, tags, and labels.
