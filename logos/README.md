# coreplane + polylane logos

Every folder holds both brands side by side: `Coreplane_*` and `Polylane_*` files. Both use
the same canvases, folder structure and variant names.

## Coreplane

The mark is "the stack": three planes in section, the middle one solid. It is the plane
between the data plane and the control plane, the one that runs itself.

Colors: ink `#15151a`, cream `#fafaf7` (RGB). CMYK files use pure black and white for print.
Wordmark: Geist Mono SemiBold (600), converted to outlines, so no font is needed to use
these files.

## Polylane

The mark is the Polylane face: a rounded outline with a notch on top and two dot eyes. It is
the agent that lives in your production. The face is drawn with continuous curvature, so its
corners bend smoothly the way Apple's do, and its ring is an even weight all the way round.

The wordmark is "polylane" in Söhne Mono Kräftig, with the "l" redrawn to a curved shoulder.
It is converted to outlines, so no font is needed to use these files.

Proportions are measured in the wordmark's x-height:

- **Face height:** 2 x-heights, centred on the x-height band.
- **Gap:** 1 x-height between the face and the word.
- **Stacked:** the face is centred over the word, 1 x-height above the top of the "l".

At this size the face's ring is as thick as the letters' stroke, each eye is the size of the
counter in the "o", and the face spans the word from the top of the "l" to the bottom of the
"p".

Colors:

| Name | Hex | Use |
|---|---|---|
| Fern | `#29E047` | The face on light grounds |
| Fern dark | `#3FF35D` | The face on dark grounds |
| Ink | `#15151A` | Wordmark and single-color files on light |
| Cream | `#FAFAF7` | Wordmark and single-color files on dark |
| White | `#FFFFFF` | Light tile ground |
| Black | `#131416` | Dark tile ground |

Never put white or cream on Fern: on a green ground the face is ink.

## Structure

- **01_Primary:** horizontal logo (mark + wordmark).
- **02_Secondary:** mark only.
- **03_Tertiary:** stacked logo (mark above wordmark).
- **04_CMYK:** the same three, in print colors.
- **05_Social:** icon and full-logo tiles with the ground baked in, plus Coreplane's platform
  covers. Polylane's profile headers and avatars live in [`social/`](../social).

## Variants

- **LightBg / DarkBg:** which ground the file is meant for. The background is transparent and
  the ink flips: ink on light, cream on dark.
- **Flat:** the top plane is filled with the named ground color. Use it only on that ground.
- **Neutral:** single color throughout, with a true cutout interior. Safe over any surface:
  photos, gradients, unknown grounds.

On its named ground, Flat and Neutral look identical. The Polylane face has a true cutout
interior, so its Flat and Neutral files are the same drawing. Both are kept so every variant
name exists for both brands.

Polylane also ships a **Primary** color variant of every file: the face in Fern (`#29E047`
on LightBg, `#3FF35D` on DarkBg) with the wordmark in the ground's foreground color. CMYK
folders carry the same greens as placeholders for a spot color; no print match has been
chosen yet.

Polylane's icon tiles (`05_Social/01_Icon`) are drawn like its avatars: the face is 60% of
the tile wide and centred.

- **DarkBg / LightBg:** cream face on black, ink face on white.
- **DarkBg_Primary / LightBg_Primary:** Fern face on black or white.
- **GreenBg_Black:** ink face on a Fern tile.

Its full-logo tiles (`05_Social/02_FullLogo`) centre the horizontal logo at 64% of the tile
width.

## Regenerating

SVGs are the source of truth and PNGs are rendered from them at the sizes in each folder.
Coreplane assets come from `~/coreplanelabs/coreplaneai/public/logo.svg` and are rendered with
`rsvg-convert`. Polylane files are generated from the brand masters (the face and the outlined
wordmark) by a script, and rendered with resvg.
