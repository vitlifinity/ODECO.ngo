# Global Academy — Equipped for Life &amp; Ministry

One-page marketing site for Global Academy's 2026/2027 course catalogue
(Spiritual Equipment Seminary). Static HTML — no build step.

## Structure

```
.
├── index.html          # the entire site (HTML + inline CSS/JS)
├── assets/             # local images
│   ├── global-academy.jpg
│   ├── odeco-logo.png
│   ├── hvac-outdoor-unit.png
│   └── electrical.jpg
└── vercel.json         # static hosting config (caching + clean URLs)
```

Fonts (Google Fonts), the QR generator, and four course photos load from
public CDNs, so an internet connection is required when viewing.

## Run locally

Just open `index.html` in a browser, or serve the folder:

```bash
npx serve .
# or
python3 -m http.server 5173
```

## Deploy to Vercel

**Option A — CLI**

```bash
npm i -g vercel
vercel          # preview deploy
vercel --prod   # production
```

**Option B — Git import**

1. Push this folder to a GitHub/GitLab/Bitbucket repo.
2. In Vercel: *New Project → Import* the repo.
3. Framework preset: **Other**. Build command: *(none)*. Output dir: `./`.
4. Deploy.

## Push to Git

```bash
git init
git add .
git commit -m "Global Academy one-page site"
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main
```

## Editing

- **Registration link** — update the Google Form URL in `index.html`
  (search `docs.google.com/forms`); it is wired to every "Register" button
  and the QR code.
- **Contact** — phone/name live in the `#register` section.
- **Courses** — each course is an `<article class="card">` in the
  `#courses` grid.
