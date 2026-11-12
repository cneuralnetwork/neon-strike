# Neon Strike

A wave-survival first-person shooter that runs in the browser. Everything you see and hear is generated in code at load time: the map, the textures, the weapons, the enemies and the audio. There are no model, image or sound files.

**Play it:** https://neon-strike-fps-pc9z.netlify.app

## How to play

| Input | Action |
| --- | --- |
| W A S D | Move |
| Mouse | Look (click Play to capture the pointer) |
| Left click | Fire |
| Right click | Aim down sights |
| Space | Jump |
| Shift | Sprint |
| C or Ctrl | Crouch |
| R | Reload |
| 1 2 3 or mouse wheel | Switch weapon |
| F | Fullscreen |
| Esc | Pause |

Survive waves of combat androids. The shotgun unlocks at 500 points and the bolt-action rifle at 1500. Every fifth wave brings a boss. Red barrels explode when shot.

Built for desktop browsers with a keyboard and mouse. If it runs slowly, set graphics quality to Medium or Low in Settings.

## Features

- **Rendering:** Three.js with a shadow-casting sun, image-based lighting from a procedural sky, physically based materials, bloom, ACES tone mapping, film grain and FXAA.
- **Textures:** concrete, cracked wet asphalt, corrugated steel and riveted plate, generated with tiling fractal noise into colour, normal and roughness maps.
- **Weapons:** carbine, pump shotgun and bolt-action rifle, each with its own recoil pattern, reload animation, shell ejection and synthesized sound.
- **Feel:** spring-based camera and weapon kick, weapon sway and bob, landing impact, near-wall weapon pull-back, coyote-time jumping.
- **Enemies:** articulated androids driven by a state machine (chase, attack, take cover, retreat), flow-field pathfinding and Verlet ragdolls on death.
- **Effects:** GPU particle sparks and smoke, bullet-hole decals, ricochets, chain-reacting explosive barrels and scorch marks.
- **Audio:** layered Web Audio synthesis with a convolution reverb tail, positional enemy fire and footsteps that change with the surface.

## Run locally

It is a single static page. Serve the folder with any static server:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000. Opening `index.html` directly from disk also works in most browsers.

Three.js r128 and its post-processing examples load from cdnjs and jsDelivr, and fonts load from Google Fonts, so the page needs a network connection.

## Deploy

The repo includes a `netlify.toml` that publishes the folder as is, with no build step. Any static host works.

## Licence

MIT. See [LICENSE](LICENSE).
