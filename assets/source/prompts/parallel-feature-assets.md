# Parallel Feature Asset Handoff

Use the existing art direction in `assets/source/prompts/style-bible.md` and the current runtime assets as visual references. Produce runtime-ready PNG or WebP files with no text, no watermark, no copyrighted characters, and no UI labels. Keep all action readable on a mobile canvas for a 3 to 4 year old.

## Court Backgrounds

Create separate portrait and landscape runtime backgrounds for each court ID. Keep the lower third clear enough for the dino, ball, hoop, and controls.

- `jungle`: bright friendly dino basketball court with soft leaves and playful prehistoric shapes.
- `beach`: sunny beach basketball court with sand, water, shells, and palms kept away from the main ball path.
- `volcano`: cheerful cartoon lava-rock court with warm glow, no scary danger, and clear open sky for shot arcs.
- `space`: moon court with stars, planets, and soft low-gravity motifs, still bright enough for a toddler game.

Target runtime paths:

- `assets/images/backgrounds/jungle-landscape.webp`
- `assets/images/backgrounds/jungle-portrait.webp`
- `assets/images/backgrounds/beach-landscape.webp`
- `assets/images/backgrounds/beach-portrait.webp`
- `assets/images/backgrounds/volcano-landscape.webp`
- `assets/images/backgrounds/volcano-portrait.webp`
- `assets/images/backgrounds/space-landscape.webp`
- `assets/images/backgrounds/space-portrait.webp`

## Dino Pose Completion

The renderer can now swap selected dino assets by ID. Complete any missing pose files with the same side-facing ground anchor and approximate visual scale as the starter dino.

Required poses per dino: `idle`, `launch`, `happy`, `shrug`.

Target runtime paths:

- `assets/images/characters/ptero/happy.png`
- `assets/images/characters/ptero/shrug.png`

If existing trike and stego PNGs need refinement, keep their filenames and pose meanings unchanged.

## Special Shot Visuals

Create optional transparent PNG overlays or simple sprite strips for the automatic special shots. These are decorative only and should never imply a new control.

- Rainbow arc sparkle
- Moon shot comet puff
- Bank shot backboard burst
- Dunk stomp burst
- Star ball glint
- Bubble ball shine

Suggested runtime paths:

- `assets/images/effects/rainbow-spark.png`
- `assets/images/effects/comet-puff.png`
- `assets/images/effects/backboard-burst.png`
- `assets/images/effects/dunk-burst.png`
- `assets/images/effects/star-glint.png`
- `assets/images/effects/bubble-shine.png`

## Sticker Book And Badges

Create large simple icon-style stickers for the in-game sticker book. These should be readable at about 80 to 140 px wide.

- One sticker portrait per dino: trex, trike, stego, ptero.
- One court badge per court: jungle, beach, volcano, space.
- Optional small crown, star, and sparkle badges for surprise moments.

Suggested runtime paths:

- `assets/images/ui/stickers/dino-trex.png`
- `assets/images/ui/stickers/dino-trike.png`
- `assets/images/ui/stickers/dino-stego.png`
- `assets/images/ui/stickers/dino-ptero.png`
- `assets/images/ui/stickers/court-jungle.png`
- `assets/images/ui/stickers/court-beach.png`
- `assets/images/ui/stickers/court-volcano.png`
- `assets/images/ui/stickers/court-space.png`

## Hatch Assets

Create optional transparent egg sprites for unlocks. Keep them simple and friendly.

- Egg whole
- Egg cracked stage 1
- Egg cracked stage 2
- Egg shell halves

Suggested runtime paths:

- `assets/images/effects/egg-whole.png`
- `assets/images/effects/egg-crack-1.png`
- `assets/images/effects/egg-crack-2.png`
- `assets/images/effects/egg-shells.png`

## Prompt Template

Use case: stylized-concept
Asset type: mobile canvas game runtime asset
Primary request: [asset from the lists above]
Style/medium: polished 2D children game illustration, rounded chunky shapes, soft shading, cheerful color, same style as current Dino Basketball assets
Composition/framing: centered subject with generous padding, readable at small mobile sizes
Lighting/mood: bright, friendly, gentle, celebratory
Constraints: no text, no watermark, no logos, no scary expressions, no sharp realistic danger, toddler-friendly
Avoid: busy detail in gameplay lanes, dark low-contrast silhouettes, root-absolute path assumptions
