# Georgiou1226.github.io

Personal site, built with [Astro](https://astro.build), no UI framework,
plain CSS with variables for theming (light/dark automatic).

## Structure

- `src/data/projects.js` — every project shown on the site. Edit this to
  add projects, change tiers, add images, or add a link once you have a
  TDS article or write-up for something. Nothing else needs to change.
- `src/pages/` — one file per route (`index.astro` = home, `work.astro`,
  `about.astro`, `photography.astro`).
- `src/components/ProjectCard.astro` — the card used on both the
  homepage and the work page.
- `src/layouts/Layout.astro` — shared nav, footer, and page shell.
- `src/styles/global.css` — colors, type, spacing. Change the values at
  the top under `:root` to restyle the whole site.
- `public/photography/` — put photo files here, reference them from
  `src/pages/photography.astro`.

## Local development

```bash
npm install
npm run dev
```

Opens at `http://localhost:4321`.

## Deploying

A GitHub Actions workflow (`.github/workflows/deploy.yml`) builds and
deploys automatically on every push to `main`. One-time setup:

1. In the repo on GitHub: **Settings → Pages → Build and deployment →
   Source**, set it to **GitHub Actions** (not "Deploy from a branch").
2. Push to `main`. Check the **Actions** tab for build status.
3. Site goes live at `https://georgiou1226.github.io`.

No build step needed on your end, GitHub does it on every push.
