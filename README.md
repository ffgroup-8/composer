# Dream Sequence

A brand graphic generator. Drop in any royalty-free photograph and turn it into an abstract, brand-safe image: blur and liquify the photo, lay a gradient built only from brand colors over it, add grain, and export a high-resolution JPG.

Prototype. The palette is provisional until the master brand library is finalized.

## Use it

Open `index.html` in a browser (Chrome, Safari, Edge or Firefox). No install, no build step, and nothing is uploaded: the image never leaves the browser.

1. **Recipes** give a starting point. **Shuffle colors** makes a new brand-safe combination.
2. **Source**: choose or drop a photo, pick a frame shape, drag the image to reframe it.
3. **Dream**: blur, motion blur and liquify, from crystal clear to fully abstract.
4. **Color**: pick a color dot, choose its shade from the brand palette, and drag the dot on the image to place it. *Tone map* recolors the photo by brightness instead. The blend mode controls how color meets the photo.
5. **Grain**: film noise on top.
6. **Export JPG** at 2400, 4000 or 6000 px on the long edge.

## Change the brand palette

All colors live in the `BRAND` object at the top of the script in `index.html`. Replace the hex values there and every swatch, recipe and shuffle follows. The tool cannot produce a gradient color outside that list.

Recipes live in `RECIPES` just below it.
