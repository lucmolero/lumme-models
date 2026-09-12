# Lumme voice runtime decision (2026-09-12)

The launch catalog intentionally excludes Piper. Android system TTS remains the instant zero-download fallback.

| Plugin | Android runtime | Brazilian Portuguese | Voice profiles | Role |
|---|---|---|---|---|
| Kokoro fp32 1.1 | sherpa-onnx CPU | `pf_dora`, `pm_alex`, `pm_santa` | 3 | premium naturalness; larger download |
| Supertonic 3 int8 | sherpa-onnx CPU/ONNX | language `pt` (validate Brazilian accent on device) | M1-M5, F1-F5 | fast/edge profile; 128 MB |

Both packages are downloaded only from immutable HTTPS releases, verified with SHA-256, extracted with required-file validation, and kept outside the APK. `VoiceSynthesizerFactory` is the single runtime boundary and `SegmentSynthesisWorker` receives the selected plugin id, so new engines do not leak into the audiobook pipeline.

Supertonic's code is MIT and its model weights are OpenRAIL-M. The upstream repository is archived, so the release process must pin the exact asset and preserve the license notice. Kokoro uses the official Apache-2.0 model card and the fp32 Android package; int8 is not the production default because Android/ARM artifact reports were observed.
