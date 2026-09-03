# Ali Husnain — Portfolio

Personal portfolio site. Single self-contained `index.html`, no build step, no dependencies
beyond Google Fonts.

**Live:** https://ali-husnain-186.github.io/github-portfolio/

## Deploy to GitHub Pages

1. Create a new public repo named `github-portfolio` (or `Ali-Husnain-186.github.io` for a root domain).
2. Push these files to the `main` branch:

   ```bash
   git init
   git add .
   git commit -m "Add portfolio site"
   git branch -M main
   git remote add origin https://github.com/Ali-Husnain-186/github-portfolio.git
   git push -u origin main
   ```

3. Repo → **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main` / `/ (root)` → Save.
4. Wait ~1 minute, then open the URL above.

## What to edit

| What | Where in `index.html` |
| --- | --- |
| Work history (3 placeholder roles marked `edit me`) | `<section id="experience">` |
| Contact email | search for `team@receni.com` (appears 3×) |
| Stats row (3+ years, 6 projects…) | `<div class="stats">` |
| Projects | `<section id="work">` — feature card + `.proj` links |
| Accent colour | `--accent` in the `:root` block |

## CV download

The hero has a **Download CV** button pointing at `Ali-Husnain-CV.pdf`.
Your CV is already in place at that path.

## Files

```
index.html            the whole site


.nojekyll             tells Pages to serve files as-is
```
