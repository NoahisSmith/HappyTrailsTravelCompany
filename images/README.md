# Images

## Folders

- `logo/` — brand logos and favicons (the pages use the `NoText` sizes; the
  1024px and `Travel` versions are for social media / print).
- `branding/` — social network icons shown in the footer (rendered white via CSS).
- `services/` — service photos. The pages use the optimized `*-810x540.jpg`
  copies; the `*-1620x1080.png` files are the full-size originals.
- `testimonials/` — trip photos for the testimonials page (see its README).

## Loose files

- `about.jpg` — full-size About page photo (original); the page serves the
  optimized `about-web.jpg` copy.

## Remaining placeholders

| File        | Used on              | Suggested replacement                          |
|-------------|----------------------|------------------------------------------------|
| `hero.svg`  | Home hero background | A wide, scenic travel photo (landscape, ~1600×900) |

To swap `hero.svg`: add your photo (e.g. `hero.jpg`) and update the
`url("../images/hero.svg")` reference in `css/style.css`.

## Tips

- Keep page-served photos web-optimized (ideally under ~400 KB each) so the
  site loads fast on phones. Full-size originals are fine to keep in the repo —
  they just shouldn't be referenced by the pages.
- Card/service images look best around a 3:2 ratio (e.g. 810×540).
