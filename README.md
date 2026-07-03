# Irfan & Co — landing page

Temporary "work in progress" page for **Irfan & Co**, built to the brand system
(*Edition 01 — 2026*). One page, no build step, no dependencies. Drop it on
GitHub Pages and it runs.

> Status: **work in progress.** The only live link is Instagram —
> [@irfanco.media](https://www.instagram.com/irfanco.media/).

---

## Files

| File          | What it is                                                        |
| ------------- | ----------------------------------------------------------------- |
| `index.html`  | The whole page — markup, styles and the signal animation, inline. |
| `.nojekyll`   | Tells GitHub Pages to serve files as-is (skips Jekyll). Keep it.   |
| `README.md`   | This file.                                                        |

---

## Deploy on GitHub Pages

1. Create a repo and add these files at the **root** (not in a subfolder).
2. Push to `main`.
3. Repo **Settings → Pages → Build and deployment**
   → Source: **Deploy from a branch** → Branch: `main` → Folder: `/ (root)` → **Save**.
4. Wait ~1 minute. Your page is live at
   `https://<your-username>.github.io/<repo-name>/`.

To use a custom domain (e.g. `irfanco.com`) later, add it under
**Settings → Pages → Custom domain**.

Prefer the command line:

```bash
git init
git add index.html README.md .nojekyll
git commit -m "Irfan & Co — WIP landing page"
git branch -M main
git remote add origin https://github.com/<you>/<repo>.git
git push -u origin main
```

---

## Editing

Everything is in `index.html`.

- **Copy** — search for `COPY:` notes to find the headline, supporting line,
  eyebrow, status label and the services list.
- **Instagram link** — one place, on the `<a class="cta">` (`href` +
  `@irfanco.media`). It's the only link on the page by design.
- **Colours** — the four brand tokens live in `:root` at the top of the
  `<style>` block:

  | Token   | Hex       | Use                          |
  | ------- | --------- | ---------------------------- |
  | Paper   | `#F4F0E8` | background (~60%)             |
  | Ink     | `#16130D` | logo, headlines, body (~28%) |
  | Stone   | `#9A9082` | captions, rules (~7%)        |
  | Clay    | `#C0563A` | accent / spark only (≤5%)    |

- **Type** — Space Grotesk (display) + Inter (text), loaded from Google Fonts.
- **The signal strip** — the animated "noise → signal → noise" bar is the one
  signature element. Retune it in the `CONFIG` block near the bottom of the
  script (`CREST`, `SIGMA`, `SWEEP_MS`, `REST_MS`, …).

---

## Notes

- Responsive down to mobile, keyboard-focusable link, and
  `prefers-reduced-motion` respected (the signal renders as a single static
  waveform when motion is reduced).
- No analytics, no cookies, no third-party scripts beyond the Google Fonts
  stylesheet.
- This is a placeholder ahead of the full site. Keep it to the one Instagram
  link until the real thing ships. *Signal over noise.*
