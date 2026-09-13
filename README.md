# FoMaSE project website

Source for <https://fis3-fomase.github.io/> — the site for **FoMaSE** (Foundations
for Macroprogramming-based Software Engineering), a basic research project led by
PI Roberto Casadei and funded by the Italian FIS3 Starting Grant (~€1.1M,
2026–2031), hosted at the University of Bologna.

**Maintaining the site — adding papers, news, people — is documented in
[`HOWTO.md`](HOWTO.md).** This file covers how the site is put together.

## Stack

Hugo (extended) + [Hugo Blox](https://hugoblox.com) `blox-bootstrap/v5`, pulled in
as a Hugo **module** (see `go.mod` and `config/_default/module.yaml`). Deployed to
GitHub Pages by `.github/workflows/publish.yaml`. No npm, no bundler: SCSS is
compiled by Hugo Pipes and the one piece of JavaScript we add is inlined.

## How the design is customised

The site started from the `starter-hugo-research-group` template.
In the HugoBlox stack, the design is layered:

| Layer | File |
| --- | --- |
| Colour palette, light + dark | `data/themes/fomase.toml` |
| Fonts (Inter / Inter Tight / Source Serif 4 / JetBrains Mono) | `data/fonts/fomase.toml` |
| Tokens, typography, layout rhythm, navbar, cards, buttons | `assets/scss/template.scss` |
| Components (publication list, stat grid, people) + motion CSS | `assets/scss/custom.scss` |
| Block and view overrides | `layouts/partials/blocks/`, `layouts/partials/views/` |
| Motion JS | `layouts/partials/hooks/{head-end,body-end}/motion.html` |

`appearance.theme_day` / `theme_night` / `font` in `config/_default/params.yaml`
point at the two data files. `template.scss` and `custom.scss` are the theme's own
designated override hooks — the module ships both as empty stubs and imports them
last, after Bootstrap and the Wowchemy layer.

### Motion

Scroll reveals, a count-up on the homepage stat tiles, a navbar scrolled state,
and a decorative node-and-edge field behind the hero (a nod to the project's own
micro-to-macro subject).

## Local development

```sh
hugo server
```

Requires Hugo **extended** at the version pinned in
`.github/workflows/publish.yaml`. See [`HOWTO.md`](HOWTO.md#gotchas) for the SCSS
gotchas (the files are templated, and libsass shadows `min()`/`max()`).

## Licence

Content © Roberto Casadei, CC BY-NC-ND 4.0. Template code MIT — see
[`LICENSE.md`](LICENSE.md).
