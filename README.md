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

- **Photos are placeholders**: `assets/img/placeholder-avatar.svg` and
  `assets/img/placeholder-photo.svg` are used everywhere a real photo belongs (profile,
  publication figures, experience/education, the photos gallery). Once real image files
  are provided, drop them into `assets/img/` and update the `image:`/`avatar:`/`src:`
  fields in the matching `_data/*.yml` file to point at them.
- **PDFs are hosted locally now**: publication PDFs, presentation/poster PDFs, resource
  letters, and the CV all live under `assets/pdfs/` and `assets/cv.pdf` — no longer
  dependent on Google Drive share links staying valid/public. Two items (the sedaDNA
  Norway paper and the Piura talk) still link out to their original Drive URLs because
  the download kept failing; retry later if you want them local too.
- **Privacy**: this repo and the published site are fully public. Any photo added to
  `_data/photos.yml` / `assets/img/` is visible to anyone with the URL. Keep private
  photos out of this repo entirely (e.g. in a separate private album) and only add ones
  that are OK to be public.
