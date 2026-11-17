# tristanhottier.github.io

My portfolio site: engineering projects, my CV and a few things I build for fun.

**Live site: https://tristanhottier.github.io/**

## What's on the site

Projects, each with its own page:

- [Two-Stage Rocket](https://tristanhottier.github.io/projects/two-stage-rocket.html): a pneumatic stage separation system for my aerospace club, 2024-2025.
- [Fin-Controlled Rocket](https://tristanhottier.github.io/projects/fin-controlled-rocket.html): roll control with movable fins, plus a full GNC design (2025-2026).
- [Self-Landing Rocket Prototype](https://tristanhottier.github.io/projects/self-landing-rocket.html): the club's thrust-vectored landing prototype, 2025-2026.
- [Berkeley M.Eng. Capstone #161](https://tristanhottier.github.io/projects/capstone-vtol.html): Design-Build-Fly, 2026 to present. Confidential, so the page is a placeholder.
- [Black Hole Simulation](https://tristanhottier.github.io/projects/black-hole-simulation.html): a real-time general-relativistic renderer.
- [Electric Utility Vehicle](https://tristanhottier.github.io/projects/electric-utility-vehicle.html): a family build from 2018.

Also:

- Side project: [Loop Fitness](https://tristanhottier.github.io/projects/loop-fitness.html), a workout tracker app.
- The CV: `Tristan_Hottier_Resume.pdf`.
- The black hole demo at [/BH_Sim/](https://tristanhottier.github.io/BH_Sim/), which lives in a separate repo.

## Updating the site

It is plain HTML and CSS with no build step and no JavaScript. Edit `index.html`, `projects/*.html` or `style.css`, commit and push to `main`. GitHub Pages publishes it.

**CV, every quarter.** Replace `Tristan_Hottier_Resume.pdf` and keep the same filename. Then check the "Available" badge and each card against the CV.

**Project pages** are in `projects/`, named by slug:

| Slug | Project |
| --- | --- |
| `two-stage-rocket` | X4 |
| `fin-controlled-rocket` | X2 |
| `self-landing-rocket` | X3 |
| `capstone-vtol` | X1 |
| `black-hole-simulation` | X6 |
| `electric-utility-vehicle` | X7 |
| `loop-fitness` | side project, listed under "Side projects" on `index.html`, not in the grid |

Each card on `index.html` is one link to its page. Keep card and page text consistent with the fact bank. Don't add links inside a card, since nested links are invalid HTML.

**Photos** go in `assets/<slug>/`, using the same slug as the page.

- `cover.jpg` (1280x720) is the card image on `index.html`, the hero image on the page and the `og:image` (an absolute URL in the page `<head>`).
- To replace a photo, save the new file under the same name. If its pixel size changes, update `width` and `height` on its `<img>`.
- To add a photo, put it in `assets/<slug>/`. Keep it under about 350 KB, with the long side at 1600 px or less and EXIF/GPS data removed.
- Then copy an existing `<figure>` into the `<div class="gallery">` block of `projects/<slug>.html`. Point the link and `<img>` at `../assets/<slug>/file.jpg`, and set `width`, `height`, `loading="lazy"`, a real `alt` and a `<figcaption>`.
- Portrait images are not cropped. Add class `wide` to the `<figure>` for a wide image that should span two columns. Phone screenshots use `<div class="gallery phones">`.
- To find unused images, compare the folder with the page's `<img>` tags.

**Confidential and unpublished.** The X1 capstone stays confidential: keep the neutral placeholder and never add team or sponsor files. Raw source files dropped into `assets/` (see `.gitignore`) are never published.
