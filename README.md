# 🚜 Forklift Drift — Fast & Furious Warehouse Edition

A 3D forklift drifting game that runs entirely in a web browser. Drift around a detailed indoor warehouse, smash pallets, and rack up combo scores — Fast & Furious style.

## How to Play

Open `index.html` in any modern browser (Chrome, Edge, Firefox). No server required — just double-click the file.

> **Note:** `three.min.js` must be in the same folder as `index.html`.

### Controls

| Key | Action |
|-----|--------|
| `W` / `↑` | Accelerate |
| `S` / `↓` | Brake / Reverse |
| `A` / `←` | Steer Left |
| `D` / `→` | Steer Right |
| `SPACE` | Handbrake — triggers drift! |
| `C` | Toggle camera view |

## Features

### 🚜 High-Resolution Yellow Forklift
Built entirely from Three.js geometry primitives with full detail:
- Yellow-painted chassis, engine hood, counterweight and cab
- Transparent glass cab windows and overhead guard frame
- Steering wheel, dashboard with gauges, seat
- Functional mast with inner sliding rails and fork carriage
- Chrome forks that extend from the carriage
- 4 rubber tyres with chrome hub caps and 5-bolt pattern
- Working headlights (SpotLights), red tail lights, exhaust pipe
- Hydraulic cylinder visible on the mast

### 🏭 Detailed Warehouse Environment
- Concrete floor with painted yellow aisle lines and forklift safety zones
- Corrugated metal walls with horizontal beam detail
- Structural columns and roof trusses
- 9 banks of industrial fluorescent ceiling lights
- 6 rows of orange-and-blue metal racking units, 3 levels each, with random boxes
- 22 wooden pallets with stacked coloured boxes scattered around
- Loading dock with roll-up doors, safety bollards and dock bumpers

### 📷 Two Camera Views
1. **Third-Person (45°)** — Camera sits above and behind, following the forklift smoothly
2. **Cockpit / FPV** — Operator eye position with yellow pillar overlay, dashboard strip, and steering wheel silhouette

### 🏎️ Arcade Drift Physics
- Arcade-style velocity-blending physics with forklift rear-wheel-steer oversteer
- Handbrake cuts grip to ~7% for wild, controllable drifts
- Speed-sensitive grip: grip decreases at higher speeds enabling natural oversteer
- Top speed ~54 km/h; reverse available

### 🔥 Drift Scoring
- Score accumulates while actively drifting (angle > 8°, speed > 3 m/s)
- Drift multiplier increases with drift duration (×1.0 → ×1.5 → ×2.0 …)
- Score is banked when drift ends, shown as a floating popup
- **+150 PALLET SMASH!** bonus when hitting a pallet while drifting
- Tyre smoke particle effect during drifts

## Screenshot

Loading screen:

![Loading Screen](https://github.com/user-attachments/assets/8857a843-0328-42cc-8e90-316674024d38)

## Technical Stack

- **Rendering:** [Three.js r128](https://threejs.org/) (bundled — no CDN required)
- **Physics:** Custom arcade drift model with velocity blending
- **All geometry:** Procedural — no external 3D model files
- **Single file:** Everything is in `index.html` + `three.min.js`
