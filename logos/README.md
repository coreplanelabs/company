# coreplane + polylane logos

The mark is "the stack": three planes in section, the middle one solid — the plane
between the data plane and the control plane, the one that runs itself.

Colors: ink `#15151a`, cream `#fafaf7` (RGB). CMYK files use pure black/white for print.
Wordmark: Geist Mono SemiBold (600), converted to outlines — no font needed to use these files.

Every folder holds both brands side by side: `Coreplane_*` and `Polylane_*` files.
Polylane keeps the same metrics but its mark is the Polylane avatar: the companion face
(speech bubble, two dot eyes) that the console and docs use as favicon and app icon. The
face sits in the same 64-unit slot the stack occupies, so lockup widths, gaps and the
wordmark position are unchanged. Its path data is copied verbatim from `nominal`
(`packages/logos/polylane-face.ts`, the `dots` face). The polylane wordmark is one
monospace character shorter than coreplane's, so its lockups are 24 units narrower and
recentered.

## Structure

- **01_Primary** — horizontal lockup (mark + wordmark)
- **02_Secondary** — mark only
- **03_Tertiary** — stacked lockup (mark above wordmark)
- **04_CMYK** — the same three, in print colors
- **05_Social** — baked-background icon and full-logo tiles (both brands), plus
  platform covers. `03_Covers` also holds polylane covers (`polylane_*_cover.png`):
  identical to the coreplane ones — same mark, scale, and centering — with the
  wordmark reading "polylane". The polylane full-logo tiles follow the same rule:
  same mark scale as coreplane, shorter lockup recentered.

## Variants

- **LightBg / DarkBg** — which ground the file is meant for. Transparent background;
  the ink flips (ink on light, cream on dark).
- **Flat** — the top plane is filled with the named ground color. Use only on that ground.
- **Neutral** — single color throughout; the top plane is a true cutout (transparent
  interior). Safe over any surface: photos, gradients, unknown grounds.

On its named ground, Flat and Neutral look identical. The polylane face is a single
colour with a true cutout interior, so its Flat and Neutral files are the same drawing;
both are kept so every variant name exists for both brands.

Polylane also ships two colour variants of every face file, next to Flat/Neutral:

- **Primary** — the face in brand green `#A8E840`; the wordmark keeps the ground's
  foreground (ink on LightBg, cream on DarkBg). CMYK folders carry Primary as a spot
  colour; they have no Gradient.
- **Gradient** — the face filled with a linear gradient from `#B5FF3D` to `#54B86A`,
  running from the top-right corner of the face's bounding box towards the bottom-left
  (the end point sits 1.54 box widths left and 1.54 box heights below the start, so the
  face shows the first two thirds of the ramp), plus a 16% grain texture masked to the
  face. Geometry, stops and grain are taken from the brand's gradient lockup; the grain
  is an embedded raster, which is why these SVGs are about 2 MB.

## Regenerating

Assets are generated from `~/coreplanelabs/coreplaneai/public/logo.svg` geometry.
SVGs are the source of truth; PNGs are rendered with `rsvg-convert`.
