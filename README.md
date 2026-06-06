# farzan-portfolio

Personal portfolio site — [f4rz4n.me](https://f4rz4n.me)

Built with [Astro](https://astro.build). Deployed automatically to GitHub Pages on every push to `main`.

## Prerequisites

- Node.js v18+
- npm

## Getting started

```bash
npm install
npm run dev
```

Open [http://localhost:4321](http://localhost:4321).

## Commands

| Command         | Description                              |
| --------------- | ---------------------------------------- |
| `npm run dev`   | Start local dev server with hot reload   |
| `npm run build` | Build static output to `dist/`           |
| `npm run preview` | Preview the production build locally   |

## Project structure

```
.
├── public/
│   ├── favicon.svg          # Tab icon
│   └── CNAME                # Custom domain (f4rz4n.me)
├── src/
│   ├── layouts/
│   │   └── Layout.astro     # Root HTML shell, global CSS, fonts
│   ├── components/
│   │   ├── Navbar.astro     # Fixed top nav
│   │   ├── Hero.astro       # Landing section
│   │   ├── About.astro      # Bio and skills
│   │   ├── Projects.astro   # Project list
│   │   ├── Experience.astro # Work history and education
│   │   └── Contact.astro    # Contact links and footer
│   └── pages/
│       └── index.astro      # Entry point — assembles all sections
├── .github/workflows/
│   └── deploy.yml           # CI/CD: build → deploy to GitHub Pages
├── astro.config.mjs
└── package.json
```

## Customization

All content is co-located with its component — no separate data files or CMS.

- **Bio / skills** → `src/components/About.astro`
- **Projects** → `src/components/Projects.astro` (edit the `projects` array)
- **Work history** → `src/components/Experience.astro` (edit the `jobs` and `education` arrays)
- **Links / email** → `src/components/Contact.astro` and `src/components/Hero.astro`
- **Global colors and fonts** → `src/layouts/Layout.astro` (CSS custom properties in `:root`)

## Deployment

Pushing to `main` triggers the GitHub Actions workflow in `.github/workflows/deploy.yml`, which builds the site and deploys it to GitHub Pages.

**One-time setup** (if not already done):
1. Go to repo **Settings → Pages**
2. Set source to **GitHub Actions**

The custom domain is configured via `public/CNAME`. If you change the domain, update `site` in `astro.config.mjs` as well.

## Tech stack

- [Astro](https://astro.build) — static site generator
- Vanilla CSS (no framework)
- IBM Plex Mono + Inter (Google Fonts)
- GitHub Actions for CI/CD
