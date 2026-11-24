# Composer

A brand graphic generator. Turn any royalty-free photograph, or a plain brand color, into abstract brand-safe imagery: blur and liquify it, lay brand color over it, add a pattern and grain, and export a high-resolution JPG or PNG.

Prototype. The palette follows the current brand colors and may still change.

Live: https://ffgroup-8.github.io/composer/

## Use it

Open the link, or open `index.html` in a browser (Chrome, Safari, Edge or Firefox). No install and no build step. Images you upload never leave the browser.

The tool opens on an empty frame that asks for a photo: **Add a photo** points to the upload and Unsplash controls, or drop an image on the frame. A new photo always opens untouched, so you see it as it is before changing anything. **Recipes** along the top are complete looks. The first chip reads **Upload** until a photo is loaded; after that it reads **Original** and takes the photo back to untouched. **Shuffle colors** makes a new brand-safe combination. Once a photo has been changed, press and hold **Hold to see original** above the image to compare. **Start over**, at the top left of the image, clears the photo and every setting and returns to the empty frame; it asks once before clearing.

The four tabs are the layers, bottom to top:

1. **Image**: the background. A photo (upload one, or search Unsplash), a solid brand color, a two-tone blend, or transparent. Pick a frame shape and drag the image to reframe it. *Image opacity* fades the photo into a brand color behind it. *Treatment* softens the photo; motion and liquify are tucked underneath for more abstract looks.
2. **Color**: a brand color layer over the background. A fold (a crisp or soft edge with color fading away from it), a gradient with draggable color dots, a two-tone blend, a solid color, or a tone map that recolors the image by brightness. The gradient library has twelve presets. With a photo loaded, each one recolors the photo in its colors (shadows take the darkest color, highlights the lightest) and adds a little softness and grain; the thumbnails show your photo in each. Without a photo, each preset is a fold. The blend mode decides how color meets the image.
3. **Pattern**: dots, lines, grid, rings or contours in one brand color. *Variation* makes the shapes grow and shrink with organic noise or with the light and dark of the image.
4. **Finish**: film grain and file format.

**Export** at 2400, 4000 or 6000 px on the long edge. Choose the Transparent background to export a pattern on its own as a PNG.

## Unsplash search

Search runs on a free Unsplash access key, set in `UNSPLASH_ACCESS_KEY` near the top of the script. The free tier allows 50 searches an hour, shared by everyone using the tool; Unsplash raises that to 5,000 at no cost if the app is approved for production (https://unsplash.com/developers). If the key is removed, the tool asks each person for their own and keeps it in their browser.

## Change the brand palette

All colors live in the `BRAND` object at the top of the script in `index.html`: `core` holds the ten brand colors and `scales` holds the shade ranges built around them. Replace the hex values there and every swatch, recipe, preset and shuffle follows. The tool cannot produce a color outside that list.

Recipes live in `RECIPES` and the gradient library in `LIBRARY`, just below it.

## Custom pattern shape

The Pattern tab can offer one custom shape. Put an SVG path and its bounding box in `SHAPE`, near `PAT_TYPES`; leave the path empty to hide the option.
