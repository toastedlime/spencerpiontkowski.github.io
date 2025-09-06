# Minimal Mistakes — Resume Starter

This is a one‑page resume starter powered by the **Minimal Mistakes** Jekyll theme. Edit `_config.yml` for profile details and `src/index.md` for content.

## Source Layout
- Source files live in `src/` (pages and assets).
- Build output is written to `_site/` (generated; do not edit).
- Configuration and tooling (e.g., `_config.yml`, `Gemfile`, `docker-compose.yml`) remain at the repo root.

## Publish on GitHub Pages
1. Create a repo (for a personal site: `<username>.github.io`; for a project: any name).
2. Upload this folder’s contents to the repo root.
3. In **Settings → Pages**, set **Source** to “Deploy from a branch” and choose your default branch and root (`/`).  
   - If this is a project site under `/your-repo`, set `baseurl: "/your-repo"` in `_config.yml`.

## Customize
- Replace `src/assets/avatar.svg` with a square headshot (e.g., 250×250) and update the path in `_config.yml`.
- Drop a real `src/assets/resume.pdf` to activate the **Download PDF** button.
- Tweak the skin with `minimal_mistakes_skin:` (e.g., `air`, `aqua`, `neon`, `noir`, `plum`, `sunrise`).

## Local preview (optional)
Run locally with either:

- Ruby: `bundle install && bundle exec jekyll serve --livereload`
- Docker: `docker-compose up`

The site serves from `src/` (configured via `source: src`) and outputs to `_site/`.

## Contributing
See `AGENTS.md` for repository guidelines (structure, style, testing, and PR expectations).
