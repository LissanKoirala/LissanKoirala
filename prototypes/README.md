# lissan.dev — portfolio prototypes

Wildly different, fully-working takes on a personal portfolio for **lissan.dev**.
Same real content, radically different design language. Open [`index.html`](index.html)
to browse them all — it's the scaffold that lets you switch between every one — or
open any file directly.

Every prototype is a single self-contained HTML file — no build step, no external
dependencies, no network calls. This whole directory deploys as-is to GitHub Pages,
Vercel, Netlify, or anywhere static (see **Deploying** below).

| # | File | Direction | Mood |
|---|------|-----------|------|
| 01 | [`01-terminal.html`](01-terminal.html) | **The Terminal** — an interactive shell; type `help`, `projects`, `open worldeval` | playful · monospace · interactive |
| 02 | [`02-editorial.html`](02-editorial.html) | **The Editorial** — Swiss-typographic print magazine | minimal · refined · typographic |
| 03 | [`03-quantum.html`](03-quantum.html) | **The Quantum Lab** — dark, animated cursor-reactive particle field, glass cards | futuristic · animated · dark |
| 04 | [`04-brutalist.html`](04-brutalist.html) | **The Brutalist** — loud neo-brutalism, hard shadows, marquee | bold · colourful · high-energy |
| 05 | [`05-orbital.html`](05-orbital.html) | **The Orbit** — projects orbit a star; click a planet to open it | spatial · canvas · interactive |
| 06 | [`06-bento.html`](06-bento.html) | **The Dashboard** — modern bento-grid overview | clean · modern · light |

Two directions were pushed further into families of five variations each:

| Family | Index | Variations |
|---|---|---|
| **Terminal** | [`terminal/index.html`](terminal/index.html) | BIOS boot, Matrix login, IRC chat, vim editor, Midnight Commander file manager |
| **Orbital** | [`orbital/index.html`](orbital/index.html) | spiral galaxy, constellation chart, atom, gravity sandbox, clockwork orrery |

## Content

All projects shown are real, drawn from [github.com/LissanKoirala](https://github.com/LissanKoirala):
WorldEval / WorldArena, Quantum Junction (QMill Peak Challenge), the SwissHacks 2026
Advisory Workbench, the CASSINI aurora-visibility build, algo, the Underground live map,
God's Eye, the Solar System simulation and Robot Vision.

No biography, employer or education claims were invented. A couple of framing lines
(e.g. "based in the UK" in the editorial version) are placeholders — confirm or cut them.

## Notes

- **Accessibility:** all six honour `prefers-reduced-motion` (animations and canvases
  stop or fall back to a static frame).
- **Theming:** the editorial and bento versions adapt to `prefers-color-scheme`.
- **Fonts:** system font stacks only, so nothing depends on Google Fonts loading. If you
  pick a direction, swapping in a webfont (e.g. Space Grotesk, Inter) is a one-line change.

## Deploying

This directory is the deploy root — nothing outside `prototypes/` is needed at runtime.

**GitHub Pages** — `.github/workflows/deploy-pages.yml` (repo root) uploads this
directory as the Pages artifact on every push to `main`. One-time setup: in the repo's
**Settings → Pages**, set **Source** to **GitHub Actions**. After that, every merge to
`main` redeploys automatically. To deploy manually, run the workflow from the **Actions**
tab (`workflow_dispatch`).

**Vercel** — `vercel.json` (repo root) sets `outputDirectory: prototypes`, so importing
this repo into Vercel just works with no build command. Connect the repo at
[vercel.com/new](https://vercel.com/new) and deploy.

**Anywhere else (Netlify, Cloudflare Pages, S3, …)** — point the host at `prototypes/`
as the publish directory; there's nothing to build.

Pick a favourite and it gets polished into the real site.
