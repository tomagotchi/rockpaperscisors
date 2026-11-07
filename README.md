# Prism Orb

A single-page interactive Three.js scene: a faceted, glassy rainbow-prism orb that breathes with a soft bloom, circled by a herd of low-poly unicorns leaving sparkle trails.

Open `index.html` in a modern browser (WebGL 2). Three.js r170 loads from jsDelivr, so there's no build step. To run it locally, serve the folder, for example with `npx serve .`.

## Interaction
- **Drag**: spin the orb. It keeps its momentum, then settles back into a slow idle rotation.
- **Tap / click the orb**: a light surge sends a burst of sparks out and makes every unicorn hop.
- **Tap a unicorn**: it leaps and does a flip.
- **Pinch / scroll wheel**: zoom. **Mouse move** (desktop): gentle parallax.

## Mobile vs desktop
- On touch or small screens the scene caps the pixel ratio at 1.5, runs bloom at half resolution, skips MSAA, and uses fewer stars, sparks and unicorns (6 instead of 7).
- If the frame rate falls below about 45 fps, the pixel ratio steps down automatically.
- The camera distance is worked out from the aspect ratio, so the whole herd fits in portrait.
- `prefers-reduced-motion` slows everything down and turns off the flips.
