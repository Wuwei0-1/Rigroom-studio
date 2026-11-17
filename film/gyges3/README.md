# The Ring of Gyges III: The Epistemic Inversion

J's script (2026-11-15), `script.txt` (text of his PDF). First film made in the 3D cartoon look: Edward's cast (after J's booth storyboard, IMG_1359) modelled as full-colour 3D characters, moved by the recorded motion from J's animated-people upload (Sophia's idle) instead of hand-keyed poses.

- `test.blend`: the opening test (Sequence One, Socrates's first line and Julian's answer, 32 s), built by `toon/shot.py` in the public repo. The file holds the motion-capture skeleton from the licensed Renderpeople upload (bones and motion only, no scan), so it stays in this private studio.
- `audio/`: the lines spoken with the series voices (Kokoro: Socrates bm_george, Julian bm_lewis, Aria af_heart, Cleon am_puck), at normal speed.
- Render job: `jobs/gyges3-test` (source `blend`).

## The full film (2026-11-16)

J approved the cartoon test. The whole script is made in four sequences (`seq1.blend` … `seq4.blend`, built by `toon/film.py`), about 21 minutes:

- `script.json`: the script parsed from J's PDF (`toon/parse_script.py`); `voices.json`: each spoken item's voice and length; `audio/eNNN.mp3`: every line and stage direction, spoken with the series voices (the Narrator, Kokoro bf_emma at 0.95, reads the sequence titles and stage directions, as in Gyges II).
- Bodies move with the recorded idle; Socrates paces in Sequence Two with the recorded walk. Gestures come from the script's notes; holograms over the table follow the stage directions (the data web, the network, the nervous system whose prefrontal cortex dims and shrinks, the crystalline Mirror Force); Socrates materializes in a shimmer and vanishes in the wind; the screens turn to dawn.
- Render jobs `jobs/gyges3-seq1` … `seq4` (Eevee, 1280×720, 8 samples, on twos).

## Revision (2026-11-16, J's six notes)

`seq1.blend` … `seq4.blend` rebuilt; render jobs `jobs/gyges3b-seq1` … `seq4`.

1. Hands and arms no longer pass into each other, the slates or the booth: every sequence was walked frame by frame with `toon/clearance.py` (`film.py --check`). Seated hands rest just clear of the thighs and stay put by an arm solve each frame; Aria's and Julian's slates lie on the table, Cleon's on his upturned palm (on the seat beside him from Sequence Three).
2. Aria sits forward, her legs clear of the bench; Socrates's arms hang clear of his robes and he stands further back from the booth.
3. The wall screens show topic pictures (network traffic, the architecture, the nervous system, the Mirror Force) that change with the conversation.
4. Explainer graphics (36, about ten minutes) cut in over the dialogue: `film/scenes.py` in the public repo. The render jobs skip the frames those graphics cover.
5. Subtitles: `gyges3.srt`, timed to the voice audio, and burned into the film.
6. Faces act the script: brows and mouth corners on their own bones, with expressions (worry, frown, clench, sorrow, wonder, warm smile...) keyed to each stage direction and line as it is said, and the camera on the face the narration describes.

## Second pass (2026-11-17)

Two narrated actions were not visible, so each now has its own close-up, and the stretch around it was re-rendered (`jobs/gyges3b-seq2-fix`, `jobs/gyges3b-seq3-fix`) and spliced into the sequence renders:

- "ARIA's fingers dance across her slate": Aria leans in and her fingers tap over the slate on the table.
- "JULIAN connects his slate to the central holographic projector": Julian leans across the table, lays his fingers on his slate while the line is spoken, and braces his other hand on his knee.

The rebuilt `seq2.blend` and `seq3.blend` differ from the rendered ones outside those stretches by at most 0.17° of joint rotation.
