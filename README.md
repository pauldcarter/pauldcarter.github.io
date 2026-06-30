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

