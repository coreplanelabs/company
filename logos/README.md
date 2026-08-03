# coreplane + polylane logos

The mark is "the stack": three planes in section, the middle one solid — the plane
between the data plane and the control plane, the one that runs itself.

Colors: ink `#15151a`, cream `#fafaf7` (RGB). CMYK files use pure black/white for print.
Wordmark: Geist Mono SemiBold (600), converted to outlines — no font needed to use these files.

Every folder holds both brands side by side: `Coreplane_*` and `Polylane_*` files.
Polylane uses the same mark and metrics; only the wordmark differs ("polylane" is one
monospace character shorter, so its lockups are 24 units narrower and recentered).
Mark-only files (Secondary, social icon) are byte-identical across the two brands.

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

On its named ground, Flat and Neutral look identical.

## Regenerating

Assets are generated from `~/coreplanelabs/coreplaneai/public/logo.svg` geometry.
SVGs are the source of truth; PNGs are rendered with `rsvg-convert`.
