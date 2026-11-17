# Dream Sequence

A brand graphic generator. Turn any royalty-free photograph, or a plain brand color, into abstract brand-safe imagery: blur and liquify it, lay brand color over it, add a pattern and grain, and export a high-resolution JPG or PNG.

Prototype. The palette is provisional until the master brand library is finalized.

Live: https://ffgroup-8.github.io/melodream/

## Use it

Open the link, or open `index.html` in a browser (Chrome, Safari, Edge or Firefox). No install and no build step. Images you upload never leave the browser.

**Recipes** along the top are complete looks. **Shuffle colors** makes a new brand-safe combination. The four tabs are the layers, bottom to top:

1. **Image**: the background. A photo (upload one, or search Unsplash), a solid brand color, a two-tone blend, or transparent. Pick a frame shape and drag the image to reframe it. *Dream* blurs, streaks and liquifies it, from crystal clear to fully abstract.
2. **Color**: a brand color layer over the background. A gradient with draggable color dots, a two-tone blend, a solid color, or a tone map that recolors the image by brightness. The gradient library has ready-made starting points. The blend mode decides how color meets the image.
3. **Pattern**: dots, lines, grid, rings, contours or notes in one brand color. *Variation* makes the shapes grow and shrink with organic noise or with the light and dark of the image.
4. **Finish**: film grain and file format.

**Export** at 2400, 4000 or 6000 px on the long edge. Choose the Transparent background to export a pattern on its own as a PNG.

## Unsplash search

Search needs a free Unsplash access key (https://unsplash.com/developers). Paste it into `UNSPLASH_ACCESS_KEY` near the top of the script to switch search on for everyone who opens the tool. Left empty, the tool asks each person for a key and keeps it in their own browser.

## Change the brand palette

All colors live in the `BRAND` object at the top of the script in `index.html`. Replace the hex values there and every swatch, recipe and shuffle follows. The tool cannot produce a color outside that list.

Recipes live in `RECIPES` and the gradient library in `LIBRARY`, just below it.
