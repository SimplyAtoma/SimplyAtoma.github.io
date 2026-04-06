# SimplyAtoma.github.io

Personal Jekyll site and blog for Hector Rodriguez Duenas.

## Local Development

1. Install Ruby and Bundler.
2. Install gems:
   - `bundle install`
3. Run the site locally:
   - `bundle exec jekyll serve`
4. Open:
   - `http://127.0.0.1:4000`

## Build

- Local production build:
  - `bundle exec jekyll build`
- Output folder:
  - `_site/`

## Configuration

Site-level settings live in `_config.yml`, including:

- `url`
- `baseurl`
- `author`
- `description`
- `header-img`
- social usernames

## Content Model

- Posts:
  - `_posts/*.markdown`
- Projects:
  - `_projects/*.md`
  - Listed on `/projects/` via `projects.html`

## Contact Form (Static Hosting)

GitHub Pages does not run PHP, so `mail/contact_me.php` is not used in production.

- Set a hosted form endpoint in `_config.yml`:
  - `contact_form_endpoint: "https://formspree.io/f/your-id"` (example)
- Keep fallback email set:
  - `contact_fallback_email: "you@example.com"`
- If no endpoint is configured, the form shows an informational fallback message with direct email.

## CI

This repo includes a GitHub Action at `.github/workflows/jekyll-build.yml` that runs `bundle exec jekyll build` on pushes to `master` and pull requests.
