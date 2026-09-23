# Escrow font files

This site's typography is set up for **Escrow** (Font Bureau / Hoefler&Co / Commercial Type,
depending on foundry release), which is a licensed commercial font — it cannot be redistributed
here automatically.

To use it:

1. Purchase/obtain a web license for Escrow (Text weights) and export/convert to `woff2`/`woff`.
2. Drop the files into this folder using these exact names (or update `css/style.css` if you rename them):
   - `Escrow-Text.woff2` / `Escrow-Text.woff` (regular, weight 400)
   - `Escrow-Text-Bold.woff2` / `Escrow-Text-Bold.woff` (bold, weight 700)
   - `Escrow-Text-Italic.woff2` / `Escrow-Text-Italic.woff` (italic, weight 400)

Until these files are added, the site gracefully falls back to `Georgia` / serif, so it will
look correct (just not pixel-identical) without them.
