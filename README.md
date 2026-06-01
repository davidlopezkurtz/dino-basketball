# Dino Basketball

A single-screen, no-fail dinosaur basketball toy for a mobile browser.

This repository currently contains the 100-basket adventure build:

- Ten sprite-backed and fallback-supported dinos, one hoop, one ball
- Tap anywhere to shoot
- High auto-aim make rate with rare soft misses
- Confetti, screen shake, squash and stretch, and Web Audio sounds
- Score persistence with defensive versioned `localStorage` loading
- Ten unlockable dinos with tap-gated hatch celebrations
- Dino names appear and are spoken when supported during the hatch reveal
- Ten courts that unlock every 10 baskets through play
- Tap-only dino picker with locked dinos shown as eggs
- A large bottom-right dino power button that charges every 3 made baskets and moves the dino during power shots
- Automatic special shots including rainbow, moon, bank, dunk, star, and bubble variants
- Court-specific celebration particles for jungle, beach, volcano, space, ice, desert, candy, city, moon, and rainbow
- Session-only surprise moments such as crown, parade, hoop sparkles, and confetti rain
- A tap-only sticker book for choosing unlocked dinos and courts
- A 100-basket finale that celebrates the adventure and lets the child keep playing
- A small parent hold reset target after 100 baskets
- Static GitHub Pages friendly files with no runtime network calls
- Local image asset repository with manifest-driven Canvas rendering and procedural fallbacks

## Run locally

Open `index.html` in a browser. For phone testing, serve the folder with any simple static server and open the local network URL on the phone.

## Visual assets

Runtime art lives under `assets/images` and is registered by `assets/manifest.js`, which exposes `window.DINO_ASSETS` without using `fetch()`. Source generations and reusable prompts are kept under `assets/source`.

The game still keeps procedural drawing fallbacks for the background, dino, hoop, ball, and score badge, so a missing image should not produce a blank canvas. The six expanded courts have distinct procedural scene fallbacks and can later be replaced with `background.<court>.portrait` and `background.<court>.landscape` manifest keys.

## Deploy to GitHub Pages

Publish the repository root from the `main` branch. The game uses a single `index.html` file plus `.nojekyll`, so there are no root-absolute asset paths to break on a project Pages URL.

## Testing a fresh save

The game intentionally saves progress in `localStorage` on the same URL. To test a fresh game after an update, open the Pages URL with `?reset=1` once. Reaching 100 baskets shows the finale; tapping continues free play, and the small reset target can be held by a parent to clear progress.

## Playtest gate

Test this on the target phone. Score should persist across reloads, powers should charge and fire without confusing normal taps, unlocks should feel delightful, and the picker or sticker book should be easy to exit.
