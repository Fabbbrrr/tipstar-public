# Credits — ODD PAIR marketing page

Rows for everything on this page. The game's own asset gate is `docs/legal/CREDITS.csv`
in the private project; this file covers the page only.

## Screens and films

| File | What it is | Source | Licence | Attribution |
|---|---|---|---|---|
| `media/trailer.mp4` | 50 s trailer, re-encoded from `shots/out/oddpair-slice-trailer.mp4` | captured in the ODD PAIR build, in engine at 1280×720 | own work | ODD PAIR project |
| `media/opening.mp4` | the opening cinematic, 49 s | `shots/out/oddpair-opening-cinematic.mp4` | own work | ODD PAIR project |
| `media/hands.mp4` | 8 s loop, converted from `shots/out/handhold-shed.gif` | in-engine capture | own work | ODD PAIR project |
| `media/*.jpg` | still frames and posters | in-engine captures under `shots/` | own work | ODD PAIR project |
| `media/shot-controls.jpg` | the controls screen | `shots/menu/pad/frame_001.22.png` | own work | ODD PAIR project |

No third-party art, audio or font files are used in the game build itself. Its art and audio are
generated in code.

## Fonts (self-hosted, `fonts/`)

| Family | File | Licence | Source |
|---|---|---|---|
| Fraunces (variable) | `fraunces-var-latin.woff2` | SIL Open Font Licence 1.1 | https://fonts.google.com/specimen/Fraunces · Phaedra Charles and Flavia Zimbardi / Undercase Type |
| IBM Plex Sans (variable) | `plex-var-latin.woff2` | SIL Open Font Licence 1.1 | https://fonts.google.com/specimen/IBM+Plex+Sans · IBM |
| Silkscreen (400, 700) | `silkscreen-400-latin.woff2`, `silkscreen-700-latin.woff2` | SIL Open Font Licence 1.1 | https://fonts.google.com/specimen/Silkscreen · Jason Kottke |

The files are the Latin subsets served by Google Fonts. The OFL permits this use; the fonts are not
renamed and the licence travels with them.

## Page code

Hand-written HTML, CSS and JavaScript in `index.html`. No framework, no build step, no tracking, no
external requests at runtime.
