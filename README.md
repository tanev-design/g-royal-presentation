# G-Royal — Company Presentation

Standalone, self-contained company profile deck. Opens on **any device** — no
local `assets/` folder required, because every image is deep-linked to a CDN.

## Live links (send these to clients)

- **Web deck:** https://g-royal-presentation.vercel.app
- **PDF:** https://g-royal-presentation.vercel.app/G-Royal-Presentation.pdf

The `index.html` file in this repo is also fully portable on its own — you can
email/message it directly and the images still load (they come from jsDelivr).

## How the media works

Images are referenced via jsDelivr CDN deep links, e.g.:

```
https://cdn.jsdelivr.net/gh/tanev-design/g-royal-presentation@main/assets/<file>
```

This is why the deck renders even when the HTML is opened by itself.

## Editing workflow

This repo is the single source of truth.

1. Edit `index.html` and/or files in `assets/`.
2. `git push` → Vercel auto-deploys the web deck.
3. New/changed images are served by jsDelivr. The CDN caches `@main` for up to
   ~12h; to force a refresh immediately, hit the matching
   `https://purge.jsdelivr.net/gh/tanev-design/g-royal-presentation@main/assets/<file>`
   URL once.
