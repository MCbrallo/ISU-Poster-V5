# AI for Astrophysics and Planetary Science

An interactive conference poster, built to be read on a screen instead of pinned to a wall. Made for the International Space University.

Open it at [mcbrallo.github.io/ISU-Poster-V5](https://mcbrallo.github.io/ISU-Poster-V5/).

## What it does

A normal poster gives you a static figure and asks you to trust it. This one lets you turn the knobs. You fly a 3D scene with the Kepler and JWST spacecraft in it, walk through the transit method on a light curve you can perturb, and run a small classifier in the browser to see how a machine separates planet candidates from false positives. The maths is typeset properly, so the equations read the way they read in a paper.

Everything runs client side. There is no server, no API key and no build step in production: the whole poster is one HTML file, one module and a folder of assets.

## About the data

The catalogue is a sample of real Kepler candidates, expanded synthetically to about 1,500 rows so the visualisations have enough points to be worth looking at. The expansion is seeded, so it produces the same catalogue every time. The named planets at the base of it are real, the copies around them are not, and nothing here should be read as a measurement.

## Running it

```bash
npm install
npm run dev
```

Then open the address Vite prints. To serve it as it is deployed, any static server pointed at the repository root will do.

## Layout

| Path | What it is |
|---|---|
| `index.html` | The poster. Structure, styles and copy |
| `index.js` | The scene, the charts and the classifier |
| `data.js` | The Kepler sample and the seeded expansion |
| `assets/` | The Kepler and JWST models, their images, and the ISU mark |

## Built with

three.js for the scene, Chart.js for the figures, TensorFlow.js for the classifier and KaTeX for the equations, all loaded from a CDN.
