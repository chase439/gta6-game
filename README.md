# Golden Coast

A small, third-person open-world browser game with a sun-soaked coastal city inspired by Vice City and GTA 6. Explore on foot, drive sports cars, complete missions, and evade police pursuits.

**[Play Golden Coast](https://chase439.github.io/gta6-game/)** - designed for a computer with a keyboard and mouse.

## Inspiration

Golden Coast was inspired by the approach behind [Saltline](https://saltline.games/), a procedural 3D browser game generated with AI. Both explore what is possible with a single HTML file, Three.js, and models, textures, and sounds generated in code. Golden Coast was developed iteratively with GitHub Copilot; Saltline was a separate, single-prompt experiment using Claude Fable 5.2. The games do not use the same AI model or have identical technology stacks.

## Technology

- **HTML, CSS, and JavaScript:** the game and interface are contained in [`index.html`](./index.html), with no build step.
- **[Three.js](https://threejs.org/) and WebGL:** procedural 3D city, characters, vehicles, lighting, shadows, ambient occlusion, and bloom.
- **[cannon-es](https://github.com/pmndrs/cannon-es):** character and vehicle physics, including raycast suspension.
- **Canvas API:** procedural textures and the minimap.
- **Web Audio API:** synthesized effects, police sirens, and the in-car synthwave radio.
- **GitHub Copilot:** AI-assisted development through iterative prompts. See [`prompts.md`](./prompts.md) for a selection of the prompts.
- **GitHub Pages:** hosting for the playable game.

The models, textures, and sounds are generated in code. Three.js and cannon-es are loaded from a CDN, so an internet connection is required even when running locally.

## How to play

Click **Enter the City** to start audio and capture the mouse. Press **Esc** to release it.

| Control | Action |
| --- | --- |
| W / A / S / D | Move on foot; accelerate, steer, or brake/reverse while driving |
| Mouse | Look around |
| Shift | Run or boost |
| Space | Jump or drift |
| F | Enter or exit a nearby car |
| R | Toggle the car radio |
| G | Toggle high and performance graphics modes |
| 1 / 2 / 3 / 4 | Start the courier, race, getaway, or taxi mission |
| X | Cancel the current mission |

Missions award in-game cash. Missions 2-4 require a car. Follow the markers and GPS guidance to reach objectives.

## Run locally

Open [`index.html`](./index.html) directly in a modern desktop browser with WebGL enabled. No local server or Python is required. An internet connection is still needed to load the libraries from the CDN.

Alternatively, if you prefer to use a local server, run this from the repository directory:

```shell
python -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000).
