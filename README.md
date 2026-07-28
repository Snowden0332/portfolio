# Owen Deule — Portfolio

This repository contains a single-page, static portfolio website (HTML/CSS/JS) hosted from the repository root (GitHub Pages). The site presents an About section, Skills, Featured Projects, screenshots, and contact information.

Live site

- The repository is set up to be served from the root and is suitable for GitHub Pages. If you publish from the main branch the site URL will be: https://owenndeule.github.io/portfolio/ (please confirm if this is the correct URL).
- Note: index.html currently contains Open Graph and social meta tags that reference "Snowden" and `https://snowden0332.github.io/portfolio/`. If that is not your intended live URL or name, update `index.html` (see "Branding & meta tags" below).

Stack

- Languages: HTML, CSS, JavaScript
- Hosting: static files (no build step required) — suitable for GitHub Pages, Netlify, or Vercel
- External assets: Google Fonts (Poppins) and Font Awesome via CDN

Repository structure

```
README.md                repo info, how-to-run, and recommended next steps
index.html               single-page site (entrypoint, metadata/OG tags)
style.css                styles and responsive rules
script.js                client behavior: menu, smooth scroll, animations, lightbox
images/                  screenshots, profile images used by the site
```

How it works

- index.html is the single entry point. It loads style.css and script.js and references the images/ folder for visuals.
- script.js initializes the mobile menu, smooth scrolling, IntersectionObserver-based reveal animations, and a lightbox modal for screenshots.
- There is no build step; changes to the files are published immediately when the branch used for Pages is deployed.

How to run locally

Preview with a simple static server (recommended):

```bash
git clone https://github.com/owenndeule/portfolio.git
cd portfolio
# Option A: Python built-in server
python3 -m http.server 8000
# Option B: Node 'serve' package
npx serve .
# Then open http://localhost:8000
```

Opening index.html directly (file://) works in many browsers but running a local server avoids CORS/local-file issues for assets.

Deploy / publish

- GitHub Pages: Settings → Pages → choose the main branch and the root (/) as the source, then save. The site will be available under `https://<your-username>.github.io/portfolio/`.
- Netlify / Vercel: connect the repository and deploy the repository root — no build required.

Concrete recommendations (high priority)

1) Branding & meta tags
   - Change the page title, Open Graph, and Twitter meta tags in `index.html` from "Snowden" and `snowden0332.github.io` to your name (Owen Deule) and the correct live URL. Also confirm and update hard-coded profile links (GitHub, email) to your preferred accounts.
   - Files to edit: `index.html` (title, meta[property='og:*'], meta[name='twitter:*'], and social links).

2) Optimize images
   - Several images are large (e.g., images/owen.png ≈ 2 MB). Compress and resize screenshots and the profile image to reduce load times and improve Lighthouse scores. Recommended targets: profile image ≤ 300 KB (prefer WebP), screenshots ≤ 200–400 KB.

3) License
   - Add a LICENSE file (MIT is common for personal portfolios) so visitors know reuse terms.

4) Replace or confirm external links
   - Some links point to `Snowden0332` and external project domains (Topmax Malawi, Essie Wigs). If these are not intended, update them to your accounts or add clarifying notes.

Optional improvements (nice-to-have)

- Add a small GitHub Actions workflow to validate site builds or to auto-deploy to gh-pages (if you prefer a dedicated branch) and/or optimize images on push.
- Add badges (license, GitHub Pages live URL, last-updated) to the top of this README.
- Add a resume PDF and a dedicated contact form backed by a service (Formspree, Netlify Forms) if you want direct messages from the site.

What I changed here

- Updated README.md to document the live site, repo structure, how to run locally, and concrete next steps for branding, image optimization, and licensing.

Next steps I can take for you (pick any)

- Update `index.html` meta tags and social links to use your name (Owen Deule) and confirm the live URL (https://owenndeule.github.io/portfolio/).
- Optimize the images in `images/` (resize + compress and replace files).
- Add a LICENSE file (MIT/Apache-2.0) and update the README with a license badge.
- Create a GitHub Action to deploy to GitHub Pages or to automatically optimize images on push.

Which of these would you like me to do next? If you want the metadata and branding update, confirm the exact site URL to use and whether to replace Snowden links with your GitHub handle `owenndeule`.