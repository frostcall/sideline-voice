# Sideline Voice

Download host for the announcer voice used by the Sideline Soundboard app: pre-recorded
announcer calls and an offline synthetic voice. The app downloads these files from this
repository's Releases after install. There is no code here.

The voice belongs to Thomas Howard, and all rights are reserved. See [LICENSE](LICENSE). The files
are licensed only for use through the Sideline Soundboard and Game Day DJ apps.

## Release layout

| release tag | assets |
|---|---|
| `calls-vN` | `voice-calls-vN.zip` (one `.m4a` per call + `voice-calls.json`), `voice-calls.json` |
| `voice-vN` | `voice-pack-vN.zip` (model, tokens, `voice-pack.json`, licence files), `voice-pack.json` |

Assets are served from stable URLs of the form
`https://github.com/frostcall/sideline-voice/releases/download/<tag>/<file>`. The app reads
the manifest first, then downloads the zip and checks every file against the SHA-256 in the
manifest.

How the packs are built and retrained is documented in the app's private repository (`docs/VOICE.md`).
