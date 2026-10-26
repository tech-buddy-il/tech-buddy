# Team images

Real portraits (`.jpg`): hila, limor, linat, razi, rotem, yonathan.
The remaining SVGs are **placeholders**. The final images are generated portraits that follow
the AI Buddy / code-left visual style (same treatment as `workshop/assets/limor.png`).

When the generated images are ready:

1. Drop them here as `<name>.jpg`, resized to 640px wide (portrait orientation; they are
   displayed with `object-fit: cover`, so faces should sit in the upper third).
2. In `index.html`, change the matching `<img src="assets/team/<name>.svg">` to `.jpg` and delete the SVG
   and, if needed, fine-tune `object-position` per person (see `--limor` / `--hila`
   modifiers in `workshop/index.html` for the pattern).

Expected files: razi, limor, linat, shai, chen, rotem, yonathan, shahar, ohad, shlomi, hila.
