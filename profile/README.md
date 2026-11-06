# Typen

**Autocorrect for every app on your desktop — 100% offline, sub-millisecond, free and open source.**

Typen is one small background service that fixes typos, homophones, punctuation, and capitalisation as you type across every application on Windows, macOS, and Linux. Nothing you type ever leaves your machine.

- **Website & Live Engine Demo**: <https://autocorrect-desktop.vercel.app>
- **Download Installers**: <https://github.com/TypenApp/typen/releases>
- **Documentation**: <https://autocorrect-desktop.vercel.app/docs>
- **Sponsor Typen**: <https://github.com/sponsors/TypenApp>

---

## Repositories in `TypenApp`

| Repository | Description |
| --- | --- |
| [**`TypenApp/typen`**](https://github.com/TypenApp/typen) | Main desktop application, OS keyboard hooks (Win32, Quartz, X11, Wayland/IBus), authenticated Local IPC, 10-screen Settings UI, cross-platform installers, and public website. |
| [**`TypenApp/language-data`**](https://github.com/TypenApp/language-data) | Global English lexicon build pipeline (166,475 words from SCOWL/ESDB), SymSpell delete-distance index, trigram context model, confusion sets, 6 domain vocabulary packs, and held-out quality benchmarks. |
| [**`TypenApp/model-resources`**](https://github.com/TypenApp/model-resources) | Optional Layer 2 on-device AI model descriptors (`grammar-onnx-int8-small`, `rewrite-gguf-q4-360m`), hardware capability profiles, and Ed25519 manifest signing tools. |
| [**`TypenApp/docs`**](https://github.com/TypenApp/docs) | Product documentation, core engine architecture specs, security & privacy guarantees, and CLI reference. |

---

## Why Typen?

- **Every application**: A low-level OS keyboard hook sees keystrokes before the application does and injects flicker-free suffix-diff replacements.
- **Nothing leaves your computer**: A 166k-word lexicon is memory-mapped from disk (`mmap`) and queried in under a millisecond. Zero keystroke logging, automatic password-field exclusion, and zero telemetry.
- **Reversible by design**: Every correction is a transaction. Press `Backspace` twice immediately after a correction to restore your original word and queue it for your personal dictionary.
- **Free forever**: MIT-licensed with a single edition, no trial, no licence key, and no paid tier.
