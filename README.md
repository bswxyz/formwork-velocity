# Dev-tool startup template — animated code review

**Live demo → https://bswxyz.github.io/formwork-velocity/** · [How it was built](https://bswxyz.github.io/formwork-velocity/guide/)

> A crisp dev-tool landing whose hero types out a real diff and an AI review comment, live.

A free, MIT-licensed website template. Good for: **developer tools, APIs, CLIs, technical SaaS**.
The demo brand ("VELOCITY") is fictional — every word and colour is meant to be replaced with yours.

## The signature technique

- Self-typing terminal/diff panel with syntax-coloured spans and an inline bot comment
- Logo marquee, monospace metrics with count-ups, animated SVG pipeline
- Snappy GSAP motion tuned for a technical audience

## Use this as your own site

This repo is a **template** — everything is plain HTML/CSS/JS with **relative paths**, so it
works under *any* repo name with zero configuration.

1. Click **Use this template → Create a new repository** (top of this page).
   **Name it whatever you like** — `my-site`, `portfolio`, anything.
2. In your new repo: **Settings → Pages → Build and deployment → Deploy from a branch**,
   then pick `main` / `/ (root)` and save. (CLI: see below.)
3. Wait ~1 minute. Your site is live at `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`.

<details>
<summary>Prefer the command line?</summary>

```bash
gh repo create my-site --template bswxyz/formwork-velocity --public --clone
cd my-site
gh api --method POST /repos/YOUR-USERNAME/my-site/pages \
  -f 'source[branch]=main' -f 'source[path]=/'
```
</details>

No build step, no dependencies to install — edit the files, push, done.
The only external requests are Google Fonts and (where used) pinned CDN copies of GSAP/three.js.

## Customize it

- The diff: hero panel lines (and the bot's finding) are editable spans in `index.html`
- Metrics: count-up targets via `data-to` attributes
- Accent: one electric blue in `:root` — swap for your brand

The `/guide/` page documents the signature technique in depth (with code) — keep it, rewrite it,
or delete the folder entirely.

## Files

```
index.html        the page
styles.css        all styling (design tokens in :root at the top)
main.js           the signature effect + motion
guide/index.html  how-it-works write-up (optional — yours to keep or delete)
```

## Built-in quality

- Works with JS disabled or a CDN failure (content is never permanently hidden)
- Respects `prefers-reduced-motion`; keyboard focus styles throughout
- Canvas/WebGL feature-detected with graceful fallbacks; devicePixelRatio capped for performance
- Responsive at phone / tablet / desktop widths

## License & credit

[MIT](LICENSE) — free for personal and commercial use, no attribution required
(a link back is always appreciated). Part of **FORMWORK** — a collection of
25 free website templates: **[the full gallery →](https://bswxyz.github.io/formwork/)**
