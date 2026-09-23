# Danish Talent Predictor — Blog

A simple, static blog for the *Danish Talent Predictor* project, built with plain HTML/CSS
(no build step) so it can be published directly with **GitHub Pages**.

## Structure

```
index.html                                   → home page / post list
posts/who-is-the-next-danish-talent.html     → the "Who Is the Next Danish Talent?" article
css/style.css                                → all styling (typography, layout, figures, table)
assets/fonts/                                → Escrow font files go here (see assets/fonts/README.md)
assets/images/                               → plots/graphics used in posts (placeholders included)
```

## Article layout

The article template (`posts/who-is-the-next-danish-talent.html`) is split into three sections:

1. **How It Works** — the model-building explanation.
2. **The Predictions** — the ranked table of predicted talents, plus a full-width chart.
3. **Under the Hood** — technical details, code snippets, and validation notes.

## Placing graphics

Figures use a shared `.figure` class with a modifier for placement, so plots can sit on either
side of the text, centered, or full-width:

```html
<figure class="figure figure--right">
  <img src="../assets/images/your-chart.png" alt="Description for accessibility">
  <figcaption>Fig. N — Caption text.</figcaption>
</figure>
```

Modifiers: `figure--left`, `figure--right` (text wraps alongside on screens ≥900px, stack on
mobile), `figure--center` (matches the text column width), `figure--full` (wider, for
at-a-glance charts like bar/ranking charts).

Replace the placeholder SVGs in `assets/images/` with your real exported plots (PNG/SVG/JPG all
work — just update the `src`).

## Predictions table

Update the `<table class="predictions">` rows in the article with live model output (rank,
player, club, position, age, breakout probability). The `<span class="badge">` wrapper on the
probability column is purely a styling hook.

## Font

Typography is set up for **Escrow**, a licensed commercial serif. See
[`assets/fonts/README.md`](assets/fonts/README.md) for how to add the font files — the site
falls back to Georgia/serif until they're added, so nothing is broken in the meantime.

## Publishing to GitHub Pages

1. Push this repository to GitHub.
2. In the repo settings, go to **Pages** → set source to the `main` branch, root folder.
3. The site will be published at `https://<username>.github.io/<repo>/`.

No build tooling, Jekyll config, or dependencies are required — it's plain static HTML/CSS.
