# NestGenie.uk — TODO

## Images to replace with commissioned / owned photography

All current placeholder images are sourced from Wikimedia Commons under Creative
Commons licences. They must be replaced with original or properly licensed
photography before commercial launch.

### Current placeholder images

| File | Used on | Subject | Photographer | Licence | Source |
|---|---|---|---|---|---|
| `assets/img/hero-home.jpg` | Homepage hero | Blue tit perched at a bird box | Tony Alter | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/) | [Wikimedia](https://commons.wikimedia.org/wiki/File:Blue_tit_(7250693246).jpg) |
| `assets/img/hero-products.jpg` | Products hero | Blue tit inside a nest box | fs-phil | [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0/) | [Wikimedia](https://commons.wikimedia.org/wiki/File:Blue_Tit_-Cyanistes_caeruleus_-inside_nest_box-4.jpg) |
| `assets/img/hero-about.jpg` | About hero | Robin at Lackford Lakes | Chris Combe, York UK | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/) | [Wikimedia](https://commons.wikimedia.org/wiki/File:Robin_-_Lackford_Lakes_(31863862881).jpg) |
| `assets/img/blog-nest.jpg` | Blog post hero | Bird nest in a bush | Airwolfhound | [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0/) | [Wikimedia](https://commons.wikimedia.org/wiki/File:Bird_Nest_(3600492937).jpg) |

### What to commission

- [ ] Hero (home): Wide shot of a wooden bird box mounted on a tree or garden fence, spring foliage
- [ ] Hero (products): Clean product shot — bird box and/or nest camera on neutral/garden background
- [ ] Hero (about): Warm lifestyle shot — family or person watching a bird box in a garden
- [ ] Blog default: Atmospheric close-up of a nest with eggs, soft bokeh background
- [ ] Callout icons: Consider replacing FA icon callouts with custom illustrated icons

---

## Features / content to add

- [ ] Blog listing page (`blog/index.html`) — enables `jekyll-paginate` for future posts
- [ ] More blog posts ahead of launch
- [ ] Product detail pages (when actual products are confirmed)
- [ ] Privacy policy page (required before launch — GDPR)
- [ ] Cookie policy page (if any analytics/tracking added)
- [ ] Social sharing image (`og:image`) — 1200×630px branded card

---

## Technical

- [ ] Compress images with `jekyll-imagemagick` or pre-process before commit (hero-products.jpg is 503 KB)
- [ ] Add `alt` text to hero images once Bulma Clean Theme supports it (currently set via CSS background)
- [ ] Review `quiet_deps: true` once Bulma releases a Dart Sass 3-compatible version
