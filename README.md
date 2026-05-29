# Dino Basketball

A single-screen, no-fail dinosaur basketball toy for a mobile browser.

This repository currently contains Stage 1 of the build:

- One geometric dino, one hoop, one ball
- Tap anywhere to shoot
- High auto-aim make rate with rare soft misses
- Confetti, screen shake, squash and stretch, and Web Audio sounds
- Static GitHub Pages friendly files with no runtime network calls
- Local image asset repository with manifest-driven Canvas rendering and procedural fallbacks

## Run locally

Open `index.html` in a browser. For phone testing, serve the folder with any simple static server and open the local network URL on the phone.

## Visual assets

Runtime art lives under `assets/images` and is registered by `assets/manifest.js`, which exposes `window.DINO_ASSETS` without using `fetch()`. Source generations and reusable prompts are kept under `assets/source`.

The game still keeps procedural drawing fallbacks for the background, dino, hoop, ball, and score badge, so a missing image should not produce a blank canvas.

## Deploy to GitHub Pages

Publish the repository root from the `main` branch. The game uses a single `index.html` file plus `.nojekyll`, so there are no root-absolute asset paths to break on a project Pages URL.

## Stage 1 playtest gate

Before adding progression, dinos, courts, or persistence, test this on the target phone. The child should be able to tap, see the dino shoot, score most of the time, and want to tap again.
