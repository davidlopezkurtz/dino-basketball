# Next Graphics Roadmap

The current game has four dino IDs and four court IDs, but only the starter green dino sprite set and starter court backgrounds are real image assets. The next graphics pass should build complete sets that map directly to those runtime IDs.

## Dino Asset Sets

Create four-pose transparent sprite sets for each unlockable dino:

- `trex`: starter green dino, current baseline.
- `trike`: blue triceratops with small horns and frill, same side-facing stance and ground anchor.
- `stego`: pink stegosaurus with yellow plates, same side-facing stance and ground anchor.
- `ptero`: purple pterodactyl-inspired dino with wings, readable as a ground character for the same basketball animation.

Each dino should include `idle`, `launch`, `happy`, and `shrug` poses. Avoid relying on hue rotation for final art; use the same pose names and anchors as the starter set so the renderer can swap assets by selected dino.

## Environment Asset Sets

Create portrait and landscape backgrounds for each court ID:

- `jungle`: current bright dinosaur court.
- `beach`: sunny beach court with shells, palms, and water shapes kept outside gameplay lanes.
- `volcano`: warm lava-rock court with safe, cheerful cartoon volcano elements.
- `space`: moon court with stars, planets, and soft low-gravity visual motifs.

Each environment should keep the lower third readable for ground/court action and leave enough open sky or backdrop space for the hoop arc.

## Supporting Props

Add optional prop variants after the core dino/court sets:

- Environment-matched hoop back/front pairs for beach, volcano, and space.
- Egg sprites for each dino unlock, matching the current hatch state.
- Small picker portraits or badges for unlocked dino selection.
- Court-cycle icons for each environment.
- Particle sprites for stars, leaves, shells, sparks, and mini planets.

## Current Hoop Layering Note

The runtime hoop should stay split into:

- `prop.hoopBack`: backboard, bracket, and pole only.
- `prop.hoopFront`: rim and net only.

Do not generate a back layer that already contains a second rim/net, because the renderer draws the front layer separately after the ball.

The visible pole extension should remain responsive code, not a fixed-height bitmap, because the hoop-to-ground distance changes by viewport and safe-area layout.
