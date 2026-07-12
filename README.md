# revenant-web

The public website for [revenant](https://github.com/themsquared/revenant) —
the agent that comes back. Deployed on Netlify to **revenantai.dev**.

## Layout

- **`site/`** — the deployed static site (Netlify `publish` dir). Plain HTML/CSS/JS,
  no build step: landing page, marketplace (`/marketplace`), account onboarding
  (`/account`), plus discovery files (`llms.txt`, `llms-full.txt`, `sitemap.xml`,
  `robots.txt`).
- **`web/`** — a Vite + React app (work-in-progress console/dashboard). Not yet
  the deployed target.
- **`netlify.toml`** — publish dir, pretty-URL rewrites, security headers.

## Deploy

Netlify builds from this repo (`publish = "site"`, no build command). Pushing to
`main` triggers a deploy.

The marketplace and account pages talk to the Necropolis directory API
(`https://necropolis.revenantai.dev`), which lives in
[revenant-necropolis](https://github.com/themsquared/revenant-necropolis).
