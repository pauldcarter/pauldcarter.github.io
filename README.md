# pauldcarter.github.io

My portfolio / CV hub. Because this repo is named exactly `pauldcarter.github.io`,
GitHub Pages publishes it at the **root** URL:

**https://pauldcarter.github.io/**

The main page is a hub: hero + intro, then a tile per project and three
"deep-dive" tiles. The detail lives in sub-pages — one page per project
(features, uniqueness and the stack with the *why* for each choice) and three
comparison pages for hosting, front/back ends and storage.

## Files

- `index.html` — hub: hero + project tiles + deep-dive tiles.
- `hosting.html` — hosting platforms compared (pros / cons / limits / free tier).
- `stack.html` — front ends & back ends compared.
- `storage.html` — data stores compared, from Google Sheets to Supabase.
- `projects/*.html` — one page per project: intro, uniqueness callout, key
  features, "How it's built" fact cards.
- `style.css` — shared styling for all pages; tables and tiles reflow to
  stacked cards on mobile.

## Editing

- **Add a project:** copy a `projects/*.html` page and edit it, then copy a
  `<a class="tile">` block on `index.html` and point it at the new page. Tiles
  are single links — nothing inside a tile may be an `<a>`.
- **Comparison tables:** each row is a `<tr class="project">`; each data cell
  has a `.val` (headline) and a `.why` (muted reasoning). Keep the
  `data-label="…"` attributes — they drive the mobile stacked layout.

## Deploy

Pages builds from the `main` branch root. Commit and push to `main`; the site
rebuilds automatically.

First-time enable:

```sh
gh api -X POST repos/pauldcarter/pauldcarter.github.io/pages -f source.branch=main -f source.path=/
```

## Take it offline

The site is an on/off switch — disabling Pages stops serving it within seconds,
and the repo and its history stay intact:

```sh
gh api -X DELETE repos/pauldcarter/pauldcarter.github.io/pages   # go dark
```

Re-enable any time with the POST command above. (Pages is all-or-nothing per
site — you can't hide a single project row. Taking this hub down does not affect
the linked apps; they're hosted separately.)

