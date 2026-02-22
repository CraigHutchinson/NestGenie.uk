# Instructions for AI Assistants — NestGenie.uk

This is the **marketing website** for NestGenie, built with Jekyll and hosted on GitHub Pages at [nestgenie.uk](https://nestgenie.uk).

Read this document alongside the parent project guidelines in the NestNinja parent repository — but note the hard rule below on self-containment.

---

## Critical: Repository Self-Containment

**This repository must be fully self-contained.**

- Do **not** reference the parent management repository (`NestNinja` / the monorepo root) in any source file, link, or documentation.
- Do **not** use relative paths to sibling repositories (e.g. `../NestNinja.uk/`, `../NestNinja.pro/`).
- Do **not** reference local filesystem paths (e.g. `D:\Craig\GitHub\NestNinja`).
- Cross-brand links to `nestninja.uk` are appropriate when referencing the NestNinja upgrade ecosystem — use the `{{ site.ninja_url }}` Liquid variable (not a hardcoded URL) so local dev overrides work.

---

## Repository Purpose

**Audience:** Families, schools, first-time bird watchers, gift buyers
**Stack:** Jekyll 4.x, GitHub Pages, Minima theme (gem, solarized skin)
**Live URL:** [nestgenie.uk](https://nestgenie.uk)
**Language:** UK English throughout

---

## Brand Identity

NestGenie is the **accessible, budget-friendly** bird-watching product brand from the NestNinja family. It exists to bring nature closer to more people through carefully curated, off-the-shelf devices packaged with better guidance and convenience.

**Tagline:** *"Bring nature a little closer, every day."*
**Tone:** Warm, friendly, welcoming — this is a family brand. Write as if you are talking to a parent, teacher, or enthusiastic grandparent, not a developer or maker.
**Colour palette:** Warm purples and cream (not the NestNinja blue)

### NestGenie Is:
- A curated selection of bird-watching products (bird boxes, cameras, complete kits)
- Ready-to-use, with minimal setup required
- Budget-friendly — accessible price points (off-the-shelf equipment)
- A friendly entry point into nature watching
- A stepping stone toward the wider NestNinja ecosystem for those who want more

### NestGenie Is NOT:
- A custom hardware manufacturer — we do not design or build original hardware
- A firmware development project — no custom firmware is written for NestGenie devices
- A premium technical brand — do not position it as competing with NestNinja
- Part of the NestNinja open-source / Community Edition ecosystem
- A DIY brand — NestGenie products are ready to use out of the box

---

## Content Rules

### Tone by Page

| Page | Tone |
|---|---|
| Homepage | Warm welcome, benefit-led, inclusive |
| Products | Clear, informative, practical — help users choose |
| About | Honest, friendly, mission-focused |
| Blog | Conversational, upbeat, accessible |

### UK English
Use throughout: *colour*, *behaviour*, *licence* (noun), *recognise*, *customise*. Use `£` for pricing. Dates: DD/MM/YYYY or "February 2026" style.

### Pricing Language
- All prices are **estimates** — always qualify: `~£25 (estimated)`
- Keep pricing language approachable — emphasise value and convenience
- Do **not** compare directly with NestNinja prices (they serve a different market)
- Do **not** invent or lock in specific prices

### Product Names
- **NestGenie** — one word, capital N + capital G
- **NestNinja** — the premium sister brand (capital N + capital N), referenced only for upgrade-path context
- Do **not** call NestGenie products "DIY" or "maker" products — they are consumer-ready

### Upgrade Path Messaging
Some NestGenie-compatible devices may in future support optional upgrade paths to the NestNinja ecosystem (including the NestNinja Hub). This must be:
- Described as a **future possibility**, not a current feature
- Qualified: "where compatible hardware allows" or "on selected setups"
- Brief — not the focus of any page
- Non-technical — do not mention firmware, ESP32, or implementation details

### What NOT to Write
- Technical jargon (firmware, ESP32, PIR sensor, MIPI-CSI, etc.) — this is not the NestNinja technical site
- Any suggestion that NestGenie devices run NestNinja firmware (they do not)
- Pricing presented as final or locked in
- Internal business context (supply chain, margin, proprietary architecture)
- Anything that suggests NestGenie is lesser — it serves a different need, not a downgrade

---

## Site Structure

```
_config.yml          # Production Jekyll config
_config.local.yml    # Local dev overrides (not committed to _site)
_posts/              # Blog posts (YYYY-MM-DD-title.md)
_includes/           # Reusable partials (custom-head.html)
_layouts/            # Page templates (home.html)
_sass/               # Custom SCSS (nestgenie.scss)
assets/              # CSS (main.scss)
index.md             # Homepage
products.md          # Product range
about.md             # About NestGenie
404.md               # Error page
```

---

## Local Development

```bash
cd NestGenie.uk
bundle install
bundle exec jekyll serve --livereload --port 4002
```

Use port 4002 to avoid conflict with NestNinja.uk (4000) and NestNinja.hub (4001) when running multiple sites simultaneously.

The `_config.local.yml` override sets:
- `url: "http://localhost:4002"` (this site)
- `ninja_url: "http://localhost:4000"` (NestNinja.uk in local dev)

### Cross-Brand Links
Links to NestNinja should use `{{ site.ninja_url }}` — **never** hardcode `https://nestninja.uk`. This allows local dev cross-linking to resolve correctly.

---

## What Belongs Here

| Content | Here? |
|---|---|
| NestGenie product descriptions and pricing | ✅ |
| Brand story and mission | ✅ |
| Blog posts / product announcements | ✅ |
| Upgrade path context (brief, non-technical) | ✅ |
| Custom firmware implementation details | ❌ → NestNinja.pro |
| NestNinja premium feature descriptions | ❌ → nestninja.uk |
| Hardware schematics or BOM | ❌ → NestNinja.open |
| Open-source Community Edition content | ❌ → NestNinja.open |
| Camera feed data / Hub features | ❌ → NestNinja.hub (future) |

---

## Version

**Last Updated:** 2026-02-22
**Applies to:** NestGenie.uk repository only
**For:** Claude, GitHub Copilot, and other AI coding assistants
