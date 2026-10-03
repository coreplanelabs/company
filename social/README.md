# Social

Profile images for Polylane's accounts, and for anyone on the team who wants their profile
to match.

## Avatars

`avatars/`, 1000×1000 PNG. The face stays clear of the edges, so it survives the circle crop
every platform applies.

- `polylane-avatar-fern.png`: ink face on Fern green.
- `polylane-avatar-night.png`: Fern face on near-black.
- `polylane-avatar-constellation.png`: Fern face on near-black, in a field of colored dots.
- `polylane-avatar-made-of-dots.png`: the face drawn in colored dots on near-black.

## Headers

`headers/<platform>/`, PNG, ready to upload as they are. The layouts already keep the copy and
logo clear of the profile photo and of mobile cropping, so don't reposition them.

Each file name says which line it carries:

- `wake-up`: "Wake up to fixes, not issues."
- `on-call`: "Nobody should be on-call."

A name ending in `-logo` adds the Polylane logo. `logo-only` is the logo with no copy. Use
`company` files on Polylane's own accounts and `personal` files on your own profile.

| Platform | Where it goes | Size |
|---|---|---|
| X | Profile header | 3000×1000 (2× of 1500×500) |
| LinkedIn | Company page cover (`company`), profile background (`personal`) | 2256×382 and 3168×792 (2× of 1128×191 and 1584×396) |
| GitHub | Banner at the top of the org profile README | 2560×640 (2× of 1280×320) |
| YouTube | Channel banner | 2560×1440 |

Every file is under its platform's upload limit.

## Source

Exported from the Figma file "Polylane · Social headers". Change the design there and
re-export, rather than editing the PNGs.
