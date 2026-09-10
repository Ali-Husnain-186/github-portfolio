# Ali Husnain, Portfolio

Personal portfolio site. One self-contained `index.html` with no build step, no framework
and no dependencies beyond Google Fonts.

**Live:** https://ali-husnain-186.github.io/github-portfolio/

## What's in it

| Section | Notes |
|---|---|
| Header | Sticky, blurred, active-link underline, mobile burger menu |
| Hero | Name, role, tech row, CV download, socials, your photo in a gradient ring (embedded, no external request) |
| Stats | 2+ years, 5 roles, 6 projects, 2 stacks |
| Experience | Vertical timeline: CanDev (current), MindsTek, Artus AI, Nexthon x2 |
| Projects | Featured GameMania card with the live link, then a filterable grid. Every card has its own inline-SVG product mockup |
| Skills | Frontend, Backend and Engineering tag groups, plus Education and Languages |
| Contact | Email and LinkedIn CTA, location, phone |

## Deploy to GitHub Pages

GitHub **Actions is currently disabled** on this repo, so use branch deployment:

1. Push the files to `main`:

   ```bash
   git add index.html README.md .nojekyll
   git commit -m "Redesign portfolio"
   git push origin main
   ```

2. Repo → **Settings** → **Pages** → Source: **Deploy from a branch** →
   Branch: `main` / `(root)` → **Save**.
3. Wait ~1 minute, then open the live URL above.

## What to edit

Everything that changes lives in two JavaScript arrays near the bottom of `index.html`:

- `JOBS`: work history. Each entry has `role`, `company`, `date`, `location`, `type`,
  `desc`, `points[]`, and optional `current: true` for the "Current" pill.
- `FEATURED`: the big GameMania card, with `name`, `sub`, `desc`, `bullets[]`, `tags[]`,
  `live`, `code`, `art`.
- `PROJECTS`: the grid. Each entry has `name`, `sub`, `cats[]` (drives the filter chips
  and their counts), `desc`, `tags[]`, `url`, `meta`, `art`.
- `ART`: the inline-SVG mockups (`store`, `builder`, `canvas`, `verify`, `editor`,
  `movies`). Point a project's `art` at one of these keys, or add a new one.

Other quick edits:

| What | Where |
|---|---|
| Accent colour | `--accent` / `--accent-deep` in the `:root` block |
| Stats row | `<section class="stats">` |
| Hero photo | `#avatar`, your photo embedded as a data URI so nothing loads from outside |
| Skills / Education | `<section id="skills">` |
| Email / phone / LinkedIn | search for `Husnain.code@gmail.com` |
| CV | `Ali-Husnain-CV.pdf` in the repo root |

## Files

- `index.html`: the whole site
- `Ali-Husnain-CV.pdf`: CV linked from the hero
- `.nojekyll`: tells Pages to serve files as-is
