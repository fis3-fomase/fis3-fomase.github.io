# How to maintain this site

## Run it locally

```sh
hugo server          # http://localhost:1313, live reload
hugo --gc            # production build into public/
```

The theme is a Hugo **module** (`blox-bootstrap/v5`), pulled automatically on first
build — there is no submodule to init and no npm install. Hugo **extended** is
required (the theme compiles SCSS). CI pins the version in
`.github/workflows/publish.yaml`; keep your local Hugo on the same version.

## Publications

**Edit `publications.bib` and push. That is the whole workflow.**

On push to `main`, `.github/workflows/import-publications.yml` runs
[`academic`](https://github.com/GetRD/academic-file-converter) over the file and
opens a PR adding a page per new entry under `content/publication/`. Merge the PR
and the paper is live.

Two conventions matter:

**1. `keywords` decides where the paper appears.**

| keyword | where it shows up |
| --- | --- |
| `fomase` | on `/publication/`, and in "Latest Publications" on the homepage |
| anything else, or no keyword | nowhere in those two lists — the paper still gets its own page, and can be cited from `/details/` with the `cite` shortcode |

```bibtex
@inproceedings{Casadei2026aamas,
  title = {Macro-Programming Multi-Agent Systems: ...},
  author = {Casadei, Roberto},
  year = {2026},
  keywords = { fomase },     % <- a project output
}
```

So: add `keywords = { fomase }` to every paper that acknowledges the FoMaSE grant.
Prior work needs no keyword at all (`previous` is used on the existing entries and
is equivalent to none, as far as the page is concerned). Topical keywords are free
to use alongside — only the presence of `fomase` is tested.

To also list prior work on `/publication/`, collapsed under the project outputs,
set `show_background: true` in `content/publication/_index.md`. It is off by
default, so the page shows FoMaSE papers only.

**2. Fields prefixed with `_` are hidden from the importer.**

`_url`, `_month`, `_notes` and friends are deliberately disabled — the importer
ignores any field whose name starts with an underscore. Drop the underscore to
make a field take effect. This is how a note like "accepted for publication" is
kept in the `.bib` without it appearing on the site.

**The importer never overwrites an existing page.** Anything you hand-write into a
`content/publication/<slug>/index.md` — an abstract, a summary, extra `links:` —
survives every future import. The trade-off is that editing an entry in the `.bib`
does *not* update an already-imported page; edit the page directly, or delete it
and let the next import regenerate it.

## Adding a team member

1. Create `content/authors/<first-last>/_index.md` (copy an existing one).
2. Drop an `avatar.jpg` (or `.png`) in the same folder. Without one the site shows
   an initials monogram, so this is optional.
3. Set `user_groups`. **The string must appear verbatim in the `user_groups` list
   in `content/people/index.md`, or the person silently will not render.** Current
   groups:

   ```
   Principal Investigator · Post-docs · PhD Students · Researchers
   Grad Students · Administration · Visitors · Alumni
   ```

## Adding news

Create `content/post/<yy-mm-dd-slug>/index.md` with `title` and `date`. Put any
images in the same folder so they resolve as page resources. Posts show on `/post/`
and the three most recent appear on the homepage.

## Where things live

| What | Where |
| --- | --- |
| Homepage blocks (hero, stats, news, publications) | `content/_index.md` |
| Long-form project description | `content/details/_index.md` |
| Colour palette (light + dark) | `data/themes/fomase.toml` |
| Fonts | `data/fonts/fomase.toml` |
| Design system: tokens, type, layout | `assets/scss/template.scss` |
| Components + motion CSS | `assets/scss/custom.scss` |
| Motion JS (reveals, count-up, hero field) | `layouts/partials/hooks/body-end/motion.html` |
| Block/view overrides | `layouts/partials/blocks/`, `layouts/partials/views/` |

See `README.md` for why the theme is customised this way.

## Gotchas

- **SCSS is templated first.** Hugo runs `.scss` through its template engine before
  Sass, so `{{` and `}}` are live delimiters in those files.
- **libsass, not dart-sass.** `min()` and `max()` are Sass built-ins that shadow the
  CSS functions, and mixed-unit arithmetic (`1rem + 2vw`) must be wrapped in
  `calc()`. Both will fail the build, not degrade silently.
- **The contact map is off** because `coordinates` is commented out in
  `content/contact/index.md`. Uncomment it with real lat/long to enable it;
  `features.map.provider` in `params.yaml` is already set.
