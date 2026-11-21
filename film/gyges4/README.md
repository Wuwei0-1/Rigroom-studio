# The Ring of Gyges IV: Out of the Cave

(Working title *Whether Seen or Unseen*; J chose *Out of the Cave* on 2026-11-20.)

J's new film (2026-11-17): Julian takes the brass ring Socrates left in the lounge and is carried to the Piraeus on the night of Plato's *Republic*. He watches the whole dialogue at Cephalus's house invisible, in the cartoon style of Gyges III.

- `script.md`: the script, exported from the Docs artifact "The Ring of Gyges IV: Whether Seen or Unseen" (seven sequences, all ten books; the Athenians speak Jowett's public-domain translation, cut and condensed).
- `script.json`: the script parsed by `toon/parse_md.py` (public repo), with the speeches that run to several paragraphs listed in `/home/claude/gyges4/cont.txt`.
- `voices.json` and `audio/eNNN.mp3`: every line, stage direction and insert, spoken with Kokoro (43 minutes of speech). Series voices for Socrates (bm_george), Julian (bm_lewis), Aria (af_heart), Cleon (am_puck) and the Narrator (bf_emma at 0.95); new voices: Glaucon bm_fable, Adeimantus bm_daniel (0.97), Cephalus am_michael (0.9), Polemarchus am_liam, Thrasymachus am_fenrir (1.02), the servant boy am_echo (1.08). Greek names are respelled for the speech engine (`say_all.py`).
- `test.blend`: the first test, elements 67–74 (the start of Sequence Two: Thrasymachus bursts in, Socrates answers, "justice is nothing else than the interest of the stronger"), 81 seconds, built by `toon/athens.py`. It holds the licensed motion-capture skeleton, so it stays here. Render job `jobs/gyges4-test`.

## How the courtyard scenes are built (public repo, `toon/`)

- `athenians.py`: the new cast in Edward's style: Cephalus (bald, long white beard, garland), Polemarchus, Thrasymachus (black curls and beard, purple himation), Glaucon, Adeimantus, and the silent guests Lysias, Euthydemus, Cleitophon and Charmantides. Each wears a chiton and a himation; the long part of the skirt is its own object, hidden when the figure sits.
- `courtyard.py`: Cephalus's courtyard: plastered walls with a red dado and a painted frieze, a Doric colonnade, the altar, racks of bronze shields (the family's trade), lamp stands, chairs in a semicircle round Cephalus's cushioned chair, a bench, and the gate to the street.
- `athens.py`: the director: who sits or stands where, recorded idle motion, gaze, faces from the script's notes, gestures, Julian as a glassy outline with no shadow while the ring is turned inward, cameras and cuts. `--check N` walks the scene with `clearance.py`; `--check 1 --lab 1` measures the base and gesture poses.
- Socrates does not wear the ring in this film; Julian does (`cast.RING_ON`).


## The finished film (2026-11-20)

`ring-of-gyges-iv.mp4`: 46 min at 1280×720, 24 fps, −16 LUFS, subtitles burned in; `gyges4.srt` alongside. Sent to J in the chat (LFS uploads from the sandbox are refused, so the joined film is not stored here; rebuild it with `film/finish4.sh` in the public repo).

- `seq1.blend` … `seq7.blend`, render jobs `jobs/gyges4-seq1` … `seq7`, results `out/gyges4-seq1` … `seq7`. Seq 1 has the lounge at dawn (`toon/lounge4.py`), the Piraeus (`toon/piraeus.py`) and the arrival at the courtyard; Seq 7 ends in the lounge.
- `gfx/`: the eleven story graphics (`film/scenes4.py`, 8 min 48 s) and `graphics.json` (where each cuts in). The render jobs skip their frames.
- `plans/`: each sequence's plan (items, cues, cuts) and `phrases.json` (word timings), which time the graphics and subtitles.
- Title card *The Ring of Gyges IV / Out of the Cave*; end card *wuwei0-1.github.io/Wuwei01*.
- YouTube thumbnail: the Design artifact *Ring of Gyges IV thumbnail* (the cave from the story graphic, with the title).
- Known: Thrasymachus's right forearm sinks a few centimetres into his belly when he sits for long stretches.
