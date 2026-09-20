# renatodltr.github.io

Personal academic website, built with [Jekyll](https://jekyllrb.com/) (natively supported by
GitHub Pages — no build step needed, GitHub builds it on every push).

## How it's organized

- `_data/*.yml` — all the actual content (profile, experience, education, publications,
  presentations, awards, resources, photos). **This is what changes over time.**
- `_layouts/default.html`, `_includes/` — shared page shell, nav, footer.
- `index.html`, `publications.html`, `awards.html`, `photos.html`, `resources.html` — the
  pages themselves; they just loop over the data files above.
- `assets/` — CSS, JS, images.

To update content (new publication, new award, edited bio, etc.), edit the matching
`_data/*.yml` file — no HTML editing needed for routine updates.

## Publishing

1. Push to the `main` branch of this repo (`RenatoDLTR.github.io`).
2. In the repo's **Settings → Pages**, set the source to "Deploy from a branch", branch
   `main`, folder `/ (root)`.
3. GitHub builds the Jekyll site automatically. It's live at
   `https://renatodltr.github.io/` a minute or two after each push.

## Known follow-ups

- **Profile photo**: `assets/img/profile.jpg` is referenced but not included yet — add an
  image at that path (or update `_data/profile.yml`'s `avatar` field to point elsewhere).
- **Photos page**: images are currently hot-linked from the original Google Sites CDN
  (`_data/photos.yml`). This works for now but isn't durable long-term — worth migrating
  to files under `assets/img/` in this repo eventually.
- **Privacy**: this repo and the published site are fully public. Any photo added to
  `_data/photos.yml` / `assets/img/` is visible to anyone with the URL. Keep private
  photos out of this repo entirely (e.g. in a separate private album) and only add ones
  that are OK to be public.
- **CV**: currently links out to the existing Google Drive PDF. Can be replaced with a
  PDF committed directly to this repo (e.g. `assets/cv.pdf`) if preferred.
