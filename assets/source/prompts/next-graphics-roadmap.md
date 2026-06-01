# Next Graphics Roadmap

The current game now has complete first-pass runtime art for 10 dino sprite sets and 10 court IDs. The next graphics pass should refine supporting variants that map directly to the 10-level progression.

## Dino Asset Sets

Refine four-pose transparent sprite sets for each dino:

- `trex`: starter green dino, current baseline.
- `trike`: blue triceratops with small horns and frill, same side-facing stance and ground anchor.
- `stego`: pink stegosaurus with yellow plates, same side-facing stance and ground anchor.
- `ptero`: purple pterodactyl-inspired dino with wings, readable as a ground character for the same basketball animation.
- `velociraptor`: teal raptor with amber crest and visible raised sickle claws on both feet.
- `spinosaurus`: orange body with aqua back sail.
- `pachycephalosaurus`: yellow body with rounded dome head.
- `ankylosaurus`: bronze low armored body with club tail.
- `parasaurolophus`: mint body with a large backward coral head crest.
- `brachiosaurus`: periwinkle long-neck body with small high head.

Each dino includes `idle`, `launch`, `happy`, and `shrug` poses. Avoid relying on hue rotation for final art; use the same pose names and anchors as the starter set so the renderer can swap assets by selected dino.

## Environment Asset Sets

Refine portrait and landscape backgrounds for each court ID:

- `jungle`: current bright dinosaur court.
- `beach`: sunny beach court with shells, palms, and water shapes kept outside gameplay lanes.
- `volcano`: warm lava-rock court with safe, cheerful cartoon volcano elements.
- `space`: moon court with stars, planets, and soft low-gravity visual motifs.
- `ice`: snowy glacier court with blue ice cliffs and warm readable court markings.
- `desert`: canyon court with red rocks, mesas, and sunlit sand kept outside the play lane.
- `candy`: candy-land court with gumdrop hills and decorative sweets outside the play lane.
- `city`: playful rooftop or schoolyard court with dinosaur-town shapes in the distance.
- `moon`: lunar base court with rounded rocks, stars, and sci-fi props kept behind the court.
- `rainbow`: sky-island court with clouds, balloons, and soft rainbow lighting.

All 10 environments now have first-pass background pairs. Future revisions should keep the lower third readable for ground/court action and leave enough open sky or backdrop space for the hoop arc.

## 10-Level Pairing

- Level 1: `trex` on `jungle`.
- Level 2: `trike` on `beach`.
- Level 3: `stego` on `volcano`.
- Level 4: `ptero` on `space`.
- Level 5: `velociraptor` on `ice`.
- Level 6: `spinosaurus` on `desert`.
- Level 7: `pachycephalosaurus` on `candy`.
- Level 8: `ankylosaurus` on `city`.
- Level 9: `brachiosaurus` on `moon`.
- Level 10: `parasaurolophus` on `rainbow`.

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
