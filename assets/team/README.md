# Team images

Portraits for the homepage team section (`#team` in `index.html`): hila, limor, linat,
razi, rotem, shahar, yonathan.

They are drawn in the AI Buddy / code-left visual style (same treatment as
`workshop/assets/limor.png`).

To add a person:

1. Save the portrait here as `<name>.jpg`, resized to 640px wide. Cards crop with
   `object-fit: cover` at `center 22%`, so keep the face in the upper part of the image.
2. In `index.html`, copy an existing `.b-team-card` block inside `.b-team__grid` and change
   the LinkedIn link, `aria-label`, image `src`/`alt`, name and role.
