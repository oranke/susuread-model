Model files for the SusuRead on-device AI voice. The app downloads these six files and checks each SHA-256.

| File | Bytes | SHA-256 |
|---|---:|---|
| `duration_predictor.int8.onnx` | 3,700,147 | `c3eb91414d5ff8a7a239b7fe9e34e7e2bf8a8140d8375ffb14718b1c639325db` |
| `text_encoder.int8.onnx` | 36,416,150 | `c7befd5ea8c3119769e8a6c1486c4edc6a3bc8365c67621c881bbb774b9902ff` |
| `vector_estimator.int8.onnx` | 78,400,833 | `20cd86fa5c6effedfda0e7cffe5b0569ca401c440a0c3a1d72bf39286c0db3fd` |
| `vocoder.int8.onnx` | 25,991,073 | `e923d60f53f95eb1ce235f1dc33ec56d9c057823c96fa6f8acf98f32b0da6152` |
| `tts.json` | 8,253 | `42078d3aef1cd43ab43021f3c54f47d2d75ceb4e75f627f118890128b06a0d09` |
| `unicode_indexer.bin` | 262,144 | `8402ca48e5189a8950138580b0fff64db6f072f24ac07cd54ba8b2fbb9883b30` |

- Source: Supertonic 3 (Copyright (c) 2026 Supertone Inc.), int8 files from the sherpa-onnx bundle `sherpa-onnx-supertonic-3-tts-int8-2026-05-11.tar.bz2` (SHA-256 `82fa96f91c4ef8abaae3a14a3f4153facf88bed821d1f7331cec2700f432c427`). Extracted byte for byte, not modified. An unchanged copy of that bundle is in the release `upstream-sherpa-onnx-2026-05-11`.
- License: **BigScience Open RAIL-M** — see `LICENSE`. **Use restrictions (paragraph 5 · Attachment A) apply**, including the duty to disclose machine-generated content (Attachment A (e)). See `NOTICE`.
- This release is immutable. The tag name matches the model ID the app uses.
