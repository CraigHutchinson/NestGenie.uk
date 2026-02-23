# NestGenie.uk

Warm, approachable bird-watching products for homes, gardens, and schools.

This repository is a GitHub Pages Jekyll site for the NestGenie placeholder launch.

## Local development

### Prerequisites
- Ruby and Bundler

### Setup

```bash
bundle install
bundle exec jekyll serve --livereload --livereload-port 35731 --port 4002 --config _config.yml,_config.local.yml
```

Visit `http://localhost:4002`.

## Current structure

- `index.md` - homepage (Bulma Clean `page` layout with hero + callouts)
- `products.md` - product line overview
- `about.md` - brand and mission
- `assets/css/app.scss` - Bulma CSS with nature-green `$primary` override
- `_data/navigation.yml` - top navigation
- `_data/genie_callouts.yml` - home page callout cards
- `_data/genie_footer_menu.yml` - footer navigation

## Theme

Uses [Bulma Clean Theme](https://github.com/chrisrhymes/bulma-clean-theme) v1.x (gem-based).
Requires GitHub Actions for deployment (see `.github/workflows/jekyll.yml`).
