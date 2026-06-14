# LAST KNOWN POSITION — interactive flight-sim demo

A browser-based drone teleoperator demo built on [three.js](https://threejs.org/).
You launch from a mother boat, fly out over open sea, locate a stranded vessel, and
respond to a human detected in the water.

## Run it

It's a static site — no build step. Serve the folder over HTTP (ES modules and the
model loaders won't work from a `file://` URL):

```bash
cd web
python3 -m http.server 8000
# open http://localhost:8000/
```

### GitHub Pages

Push this folder to a repo and enable Pages (Settings → Pages → deploy from branch).
`index.html` is at the root, so the site works as-is. `.nojekyll` keeps Pages from
stripping the asset folders.

## Controls

| Key | Action |
| --- | --- |
| W / S | Throttle forward / back |
| A / D | Strafe left / right |
| ← / → | Yaw |
| ↑ / ↓ | Altitude |
| Drag | Mouse steer |
| Shift | Boost ×2 speed (burns fuel 2.5× faster) |

## Assets

three.js, the Orbitron font, and the water-normals texture load from CDNs. The 3D
models are bundled here:

- `Drone model/` — the player drone (OBJ)
- `Charger model/` — the launch cradle (OBJ + colour map)
- `mother boat.glb` — the launch vessel
- `Stranded Boat Model/` — the rescue target (FBX + colour map)
- `Migrant 3D model/` — the survivor in the water (FBX + textures)

© Understory Films Inc. — Lead Artist: Sepehr Samimi
