# pauldcarter.github.io

My portfolio / CV hub. Because this repo is named exactly `pauldcarter.github.io`,
GitHub Pages publishes it at the **root** URL:

**https://pauldcarter.github.io/**

It presents my shipped projects as a modern comparison matrix — projects as rows,
stack categories (front end / back end / hosting / database / uniqueness) as
columns — with the choice and the *why* in each cell. Each project links to its
live deployment (or source where not yet deployed).

## Files

- `index.html` — the page: hero + intro placeholder + the project table.
- `style.css` — modern data-grid styling; reflows to stacked cards on mobile.

## Editing

- **Add a project:** copy a whole `<tr class="project"> … </tr>` block in
  `index.html` and edit the values. Each data cell has a `.val` (headline) and a
  `.why` (muted reasoning). Keep the `data-label="…"` attributes — they drive the
  mobile stacked layout.
- **Write the intro:** replace the `INTRO PLACEHOLDER` block in the hero.

## Deploy

Pages builds from the `main` branch root. Commit and push to `main`; the site
rebuilds automatically.
