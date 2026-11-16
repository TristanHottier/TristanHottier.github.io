# tristanhottier.github.io
Static site (one landing page plus seven project pages), plain HTML and CSS, no build step and no JavaScript. Edit `index.html`, `projects/*.html` and `style.css`, commit, push to `main`; GitHub Pages publishes it. `/BH_Sim/` is a separate repo.

Quarterly update: replace `Tristan_Hottier_Resume.pdf` (same filename), then check the "Available" badge and each card against the CV.

Project pages live in `projects/` (`two-stage-rocket`=x4, `fin-controlled-rocket`=x2, `self-landing-rocket`=x3, `capstone-vtol`=x1, `black-hole-simulation`=x6, `electric-utility-vehicle`=x7, `loop-fitness`=side project, listed under "Side projects" on `index.html`, not in the grid). Each card on `index.html` is one link to its page; keep card and page text consistent with the fact bank. Do not add links inside a card (nested links are invalid).

## Photos
Each project has a folder `assets/<slug>/` (same slug as the page). `cover.jpg` (1280x720) is the card image on `index.html`, the hero image on the page and the `og:image` (absolute URL in the page `<head>`).

- Replace a photo: save the new file under the same name in `assets/<slug>/`. If its pixel size changes, update `width` and `height` on its `<img>`.
- Add a photo: put the file in `assets/<slug>/` (no tool to run; keep it under about 350 KB, long side 1600 px or less, EXIF/GPS removed), then add a `<figure>` to the `<div class="gallery">` block of `projects/<slug>.html`, copying an existing one: link and `<img>` to `../assets/<slug>/file.jpg` with `width`, `height`, `loading="lazy"`, a real `alt`, and a `<figcaption>`. Portrait images are not cropped. Add class `wide` to the `<figure>` for a wide image that should span two columns. Phone screenshots use `<div class="gallery phones">`.
- X1 (capstone) is confidential: keep the neutral placeholder, never team or sponsor files.
- Images that are in `assets/` but not used on a page are listed by comparing the folder with the page's `<img>` tags.
