# Repository Guidelines

This repository contains a static site built with Jekyll using the Minimal Mistakes theme. The source lives under `src/` and compiles into `_site/`. Keep changes focused, easy to review, and reproducible locally.

## Project Structure & Organization
- `src/`: Markdown pages (e.g., `index.md`, `404.md`), `_data/`, and `assets/` (images, PDFs).
- `_config.yml`: Global site configuration (source, theme, author, navigation).
- `_site/`: Build output; never edit or commit.
- `Gemfile`, `Gemfile.lock`: Ruby dependencies. `docker-compose.yml`: Docker dev environment.
- Add pages to `src/` with YAML front matter; place media in `src/assets/` and reference as `/assets/...`.

## Build, Test, and Development
- Ruby (local):
  - `bundle install` — install gems.
  - `bundle exec jekyll serve --livereload` — run locally at `http://localhost:4000`.
  - `JEKYLL_ENV=production bundle exec jekyll build` — production build into `_site/`.
  - `bundle exec jekyll clean` — remove cached build artifacts.
- Docker:
  - `docker compose up` — serve with live reload.
  - `docker compose run --rm -e JEKYLL_ENV=production jekyll bundle exec jekyll build` — CI‑like build.

## Coding Style & Naming
- Markdown with YAML front matter; use `layout: single`, `author_profile: true`. TOC is disabled by default; enable per page with `toc: true` if needed.
- Filenames: lowercase, hyphen‑separated (e.g., `career-highlights.md`).
- YAML: two‑space indentation; keep keys consistent with `_config.yml`.
- Assets: store under `src/assets/`; prefer optimized images and relative links like `/assets/avatar.svg`.

## Testing Guidelines
- No formal test suite. Before opening a PR:
  - Build locally (Ruby or Docker) and verify pages, links, and 404.
  - Check console for Jekyll warnings and fix broken links. Optional: run a link checker if available.

## Commit & Pull Request Guidelines
- Commits: concise, present tense (e.g., `docs: update resume summary`). Group related changes.
- PRs: include a clear description, screenshots for visual changes, and link any issues. Note config updates (e.g., `_config.yml`) explicitly.
- Keep `_site/` untouched; do not commit generated files.

## Security & Configuration Tips
- Do not include secrets. Review and set `url`, `baseurl`, and author links in `_config.yml` before publishing.
- Validate external links and PDFs; prefer HTTPS. Optimize assets to keep the site fast.
