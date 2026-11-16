# tristanhottier.github.io
Static site (one landing page plus six project pages), no build step. Edit `index.html` and `style.css`, commit, push to `main`; GitHub Pages publishes it. `/BH_Sim/` is a separate repo.
Quarterly update: replace `Tristan_Hottier_Resume.pdf` (same filename), then check the "Available" badge and each card against the CV.
Project detail pages live in `projects/` (`two-stage-rocket`=x4, `fin-controlled-rocket`=x2, `self-landing-rocket`=x3, `capstone-vtol`=x1, `black-hole-simulation`=x6, `electric-utility-vehicle`=x7). Each card on `index.html` is one link to its page; keep card and page text consistent with the fact bank.
Photos/video: use the same file on the card and on the page. Save to `assets/` (e.g. `assets/x4.jpg`), then in `index.html` find `<figure class="media" id="media-x4">` (ids `media-x2`, `-x3`, `-x1`, `-x6`, `-x7`) and replace the `<svg>` with the `<img>` shown in the HTML comment above it. Do the same in `projects/<slug>.html` (`id="media-x4"`), where the comment uses `../assets/x4.jpg`. Do not add links inside a card (nested links are invalid).
X1 (capstone) is confidential: use only a neutral image, never team or sponsor files.
