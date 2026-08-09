# Collaborative Still Life

A browser-based 3D still-life arrangement and lighting tool, built for teaching composition, form, and light. Place vessels and fruit on a tabletop, light them the way you'd light a real still life (window direction, warmth, softness, bounce card), then save, export, or print the result.

**Live:** https://hannagfield.github.io/collaborative-still-life/

## Using it

- Click an object in the **Collection** panel to set it on the table.
- Drag an object to move it; drag the background to walk around the table.
- Use the **Turn** and **Size** sliders (or **Take away**) on a selected object.
- Drag the puck in **The light** panel to set where the window is, and adjust warmth, strength, softness, and bounce card fill.
- **Save this one** keeps a plate in the browser's local storage. **Export file** / **Open file** move an arrangement as a `.json` file so it can travel between machines or be shared with students.
- **Print** renders a clean, captioned sheet for handing in or hanging up.

## Example arrangement

`examples/after-cezanne.json` is a sample composition ("After Cézanne, jug and apples") you can load with **Open file** to see the format and get a starting point.

## How it's built

Everything lives in a single `index.html` — no build step, no dependencies beyond [Three.js](https://threejs.org) loaded from a CDN. Objects are built from 2D lathe profiles (the way a vessel typology drawing works) rather than loaded model files, so the whole object library ships as plain JS arrays. See the numbered comment sections in `index.html` for how the scene, props, pointer interaction, lighting, printing, and saving are organized.

## Hosting

This repo deploys to GitHub Pages automatically via `.github/workflows/deploy.yml` on every push to `main`.
