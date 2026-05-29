# Dino Basketball

A single-screen, no-fail dinosaur basketball toy for a mobile browser.

This repository currently contains the Stage 2 progression build:

- One sprite-backed starter dino, one hoop, one ball
- Tap anywhere to shoot
- High auto-aim make rate with rare soft misses
- Confetti, screen shake, squash and stretch, and Web Audio sounds
- Score persistence with defensive `localStorage` loading
- Four unlockable cosmetic dinos with a tap-gated hatch celebration
- Four courts that unlock through play, with a tap-only court cycler
- Tap-only dino picker with locked dinos shown as eggs
- Automatic special shots including rainbow, moon, bank, dunk, star, and bubble variants
- Court-specific celebration particles for jungle, beach, volcano, and space
- Session-only surprise moments such as crown, parade, hoop sparkles, and confetti rain
- A tap-only sticker book derived from current score and unlocks, with no new save fields
- A 50-basket finale that celebrates the round and lets the child tap to play again
- Static GitHub Pages friendly files with no runtime network calls
- Local image asset repository with manifest-driven Canvas rendering and procedural fallbacks

## Run locally

Open `index.html` in a browser. For phone testing, serve the folder with any simple static server and open the local network URL on the phone.

## Visual assets

Runtime art lives under `assets/images` and is registered by `assets/manifest.js`, which exposes `window.DINO_ASSETS` without using `fetch()`. Source generations and reusable prompts are kept under `assets/source`.

The game still keeps procedural drawing fallbacks for the background, dino, hoop, ball, and score badge, so a missing image should not produce a blank canvas.

## Deploy to GitHub Pages

Publish the repository root from the `main` branch. The game uses a single `index.html` file plus `.nojekyll`, so there are no root-absolute asset paths to break on a project Pages URL.

## Testing a fresh save

The game intentionally saves progress in `localStorage` on the same URL. To test a fresh game after an update, open the Pages URL with `?reset=1` once. Reaching 50 baskets shows the finale; tapping again starts a fresh round.

## Stage 2 playtest gate

Before Stage 3 polish, test this on the target phone. Score should persist across reloads, unlocks should feel delightful, the picker should be easy to exit, and the court/dino controls should not get in the way of tap-to-shoot play.
