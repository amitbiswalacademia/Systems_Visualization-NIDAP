# System Visualization

**A 10-day GIS & spatial-systems guest studio — National Institute of Design**
Guest faculty: **Amit K Biswal** · Bachelor of Design, Industrial Design, Semester VII

This repository is the landing page and project showcase for eight student research
groups who each investigated a real-world complex system through GIS, spatial data,
and rich-picture synthesis — from airport operations to migration, aquaculture to
urban transit — grounded in the systems-thinking principles of Donella Meadows and
Edward Tufte.

🔗 **Live site:** `https://YOUR-USERNAME.github.io/REPO-NAME/` *(update this once published — see [Deploying to GitHub Pages](#deploying-to-github-pages) below)*

---

## What's in this repo

| File | Purpose |
|---|---|
| `index.html` | The main landing page — hero, intro animation, filterable project grid, light/dark theme toggle. Links out to each of the 8 story pages below. |
| `airport-system.html` | Group 1 — Airport Management System (Indira Gandhi International Airport) |
| `minds-adrift.html` | Group 2 — Minds Adrift: India's Brain Drain |
| `shrimp-coast.html` | Group 3 — The Shrimp Coast: Shrimp Aquaculture in Andhra Pradesh |
| `minecraft-progression.html` | Group 4 — Minecraft Progression Map |
| `gaza-ripple-effect.html` | Group 5 — Gaza Strip: Ripple Effect of War |
| `namma-metro-threads.html` | Group 6 — City Threads: Mapping the Patterns of Namma Metro |
| `sangam-dairy.html` | Group 7 — SANGAM: The Journey Beyond Milk |
| `vijayawada-transit.html` | Group 8 — Vijayawada Transportation System |
| `og-preview.png` | Social share preview image (1200×630) used for LinkedIn/Twitter/Facebook link cards. |
| `favicon.ico`, `favicon-16x16.png`, `favicon-32x32.png`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png` | Favicon set for browser tabs, bookmarks, and home-screen icons. |
| `site.webmanifest` | Web app manifest referencing the icon set. |
| `404.html` | Branded "page not found" page (GitHub Pages serves this automatically for unmatched URLs). |
| `robots.txt` | Search-crawler rules, points to `sitemap.xml`. |
| `sitemap.xml` | Lists every page in the site for search engines. |

**All 8 story-page files must sit in the same folder as `index.html`** — the cards on
the landing page link to them with plain relative paths (e.g. `href="airport-system.html"`),
so the site works with zero configuration as long as the filenames above are kept exactly
as listed.

---

## Deploying to GitHub Pages

1. **Create a new GitHub repository** (public, so Pages can serve it on the free tier),
   e.g. `system-visualization`.
2. **Upload every file in this folder** to the root of that repository — `index.html`,
   all 8 story pages, the favicon files, `site.webmanifest`, `404.html`, `robots.txt`,
   `sitemap.xml`, and `og-preview.png`. Keep them all at the repo root (don't nest them
   in a subfolder) so the relative links resolve correctly.
3. In the repo, go to **Settings → Pages**, and under **Build and deployment** set
   **Source** to `Deploy from a branch`, branch `main` (or `master`), folder `/ (root)`.
   Save.
4. GitHub will publish the site at:
   ```
   https://YOUR-USERNAME.github.io/REPO-NAME/
   ```
   (It can take a minute or two for the first deploy to go live.)
5. **Update the placeholder URL.** Once you know your real Pages URL, replace every
   occurrence of `https://YOUR-USERNAME.github.io/REPO-NAME/` with it in:
   - `index.html` — the `<link rel="canonical">` tag and the `og:url`, `og:image`,
     `twitter:image` meta tags near the top of `<head>`
   - `robots.txt` — the `Sitemap:` line
   - `sitemap.xml` — every `<loc>` entry
   
   This step matters most for the `og:image`/`twitter:image` tags — LinkedIn, Twitter,
   and other platforms need an **absolute URL** to fetch your preview image, so the link
   card won't render correctly until these point at your live domain. After updating,
   re-upload the changed files (a plain commit + push is enough; no build step is needed).
6. **Re-scrape the link preview.** The first time you share the URL on LinkedIn, their
   crawler caches whatever it sees. If you shared the link *before* finishing step 5,
   use the [LinkedIn Post Inspector](https://www.linkedin.com/post-inspector/) to force
   a re-fetch once the real URL is live.

No build tools, bundlers, or `npm install` are required — this is a fully static site.

---

## Local preview

Just open `index.html` directly in a browser, or serve the folder locally to avoid any
`file://` quirks:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000/
```

---

## Notes for future edits

- **Theme:** the site defaults to light mode; visitors' choice is remembered via
  `localStorage` (key `course_theme`).
- **Intro animation:** plays once per browser tab (`sessionStorage`), and is skipped
  entirely for visitors with `prefers-reduced-motion` enabled.
- **Adding or changing a project card:** edit the `GROUPS_DATA` array inside the
  `<script>` block near the bottom of `index.html` — each entry controls the card's
  title, category, description, accent color, thumbnail, and the `url` it links to.
- **Regenerating the social preview image:** `og-preview.png` was generated from a
  matching HTML template at 1200×630 — update the template and re-screenshot it if the
  title, stats, or branding change.

---

© 2026 National Institute of Design · Industrial Design Discipline
Based on the systems-thinking principles of Donella Meadows & Edward Tufte.
