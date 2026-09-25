# NY1

A [Songbird](https://tivra.com) project.

| | |
|---|---|
| Tempo | 127 BPM |
| Meter | 4/4 |
| Tracks | 12 |
| Clips | 53 |
| Plugins | 43 |
| Automation lanes | 0 |

## Tracks

- 1-Am - Tisnat_Moonrock [2023-04-26 195658]
- 3-OB-Xd 2-Group
- Audio 2-Group
- 5-Heartbeat
- 6-Farfisa V
- Audio
- Audio
- Audio
- Audio
- A-Long Reverb
- B-Short Reverb
- C-Delay - Console 1

## Layout

- `NY1.bird` — arrangement & musical intent, human-readable.
- `entities/` — content keyed by stable id (clips, plugins, automation, channels). Each file stays whole until it grows large, then transparently shards into `entities/<type>/NN.json` so merges stay size-independent.
- `spaces/` — projections that place entities (arrangement rows, mixer bus) plus per-user workspaces under `spaces/users/<id>.json` (open tabs, active tab, playback scope).
- `state/` — global project state (transport, settings, sections, …).
- `samples/` & `visuals/` — media payloads, stored in R2 (see `manifest.json`).
