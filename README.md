# Rigroom studio

Private storage for Rigroom. The app at https://wuwei0-1.github.io/Rigroom/ reads and writes this repository with your token.

- `scenes/current.json` — the scene the app opens, saved automatically.
- `models/` — the people and models your scenes use (`<fingerprint>.glb`), listed in `models/index.json`.
- `jobs/<id>/` — render jobs: `scene.glb` and `job.json`.
- `out/<id>/` — finished renders: `render.png`, or `shot.mp4` and `poster.png`, plus `result.json`.

Keep this repository **private**: it holds licensed models (Renderpeople, Mixamo and others) whose licences do not allow sharing the files.

Renders run on the public Rigroom repository's GitHub Actions, which read this repository with the `STUDIO_TOKEN` secret and write results back here. Old jobs and renders can be deleted at any time.
