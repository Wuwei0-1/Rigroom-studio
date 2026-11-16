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
