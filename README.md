# ottermathtalks.github.io

Source for the OTTER website — **Operator Theory Talks for Early Researchers** — at [ottermathtalks.github.io](https://ottermathtalks.github.io). Built with [Hugo](https://gohugo.io); every push to `main` deploys automatically via GitHub Actions in about a minute.

## Monthly maintenance

Everything routine is a markdown file under `content/`:

- **Add a talk** → `content/en/talks/YYYY-MM-DD-lastname.md` — see [HOW-TO-ADD-A-TALK.md](HOW-TO-ADD-A-TALK.md), it takes under 10 minutes.
- **Add a problem** → `content/en/problems/YYYY-MM-slug.md` (same front-matter pattern).
- **Edit a page** → the matching file in `content/en/` (English) or `content/es/` (Spanish).

Talks and problems sort themselves by date: future dates appear as upcoming, past dates in the archive. You never touch layout code for monthly content.

## Preview locally

Any Hugo ≥ 0.122 works. On the current organizer machine the binary lives at `../.tools/hugo`:

```
hugo server --source .        # if hugo is on your PATH
../.tools/hugo server --source .
```

Then open http://localhost:1313.

## Repo layout

- `content/en/`, `content/es/` — all pages, talks, and problems (markdown)
- `layouts/` — HTML templates; `static/css/otter.css` — the design system
- `archetypes/talks.md` — template used by `hugo new` for talk files
- `.github/workflows/deploy.yml` — build + deploy to GitHub Pages

Math renders via KaTeX; `\( … \)` and `$$ … $$` pass through markdown untouched (Goldmark passthrough, configured in `hugo.toml`).
