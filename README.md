# ieeevr.org Hub Site

This repository is the root hub for [ieeevr.org](https://ieeevr.org). It hosts the landing page, VGTC awards content, and a past conferences index. Individual conference years (e.g. `/2027/`) live in separate repositories.

The site is served via GitHub Pages using Jekyll 4.x as a static file server — there are no Liquid templates or Markdown pages; content is authored directly in HTML.

## Local Development

Prerequisites:

- Ruby 3.x (Jekyll 4.x is not yet compatible with Ruby 4.0)
- Bundler (`gem install bundler`)

Install dependencies:

```bash
bundle install
```

Run the site locally:

```bash
bundle exec jekyll serve --livereload
```

The site will be available at `http://localhost:4000`.

## Structure

```
index.html          # Main landing page (banner, VGTC awards, about)
PastConferences.html # Past conferences index with best-paper listings
style.css           # Site-wide styles
img/                # Shared images (banners, steering committee photos)
js/                 # JavaScript
_config.yml         # Jekyll configuration (minimal)
CNAME               # Custom domain (ieeevr.org)
```

## Common Updates

**New conference year** — update `index.html`:
- Nav bar link and text (`IEEE VR 20XX`)
- Banner image in `img/` and the `<img>` src
- Past Conferences link (`/20XX/past-conferences/`)
- VGTC awards link (`/20XX/awards/vgtc/`)
- VGTC section: conference name, location, dates, nomination deadlines

**New banner image** — add the file to `img/` and update the `<img src="...">` in `index.html`.

**VGTC nomination deadlines** — update the `<ul>` under "Nomination deadlines" in `index.html`.
