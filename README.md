# susuread-model

Model files for the on-device AI voice of **SusuRead** (수수리드), an audiobook-style reader app.
The app downloads these files from this repository's **Releases**. Speech is generated on the device. Text never leaves the device.

This repository contains no code. The model files are not committed to git. They are attached to Releases only.

## Releases

| Tag | Purpose | Assets |
|---|---|---|
| `supertonic3-int8-2026-05-11` | Files the app downloads | 6 model files · `LICENSE` · `NOTICE` |
| `upstream-sherpa-onnx-2026-05-11` | Archive: unchanged copy of the upstream bundle. The app does not download it | `sherpa-onnx-supertonic-3-tts-int8-2026-05-11.tar.bz2` · `LICENSE` · `NOTICE` |

- All releases are **immutable**: their tags and assets cannot change after publication.
- A new model gets a new tag. Old tags are never deleted, so older app versions keep working.
- The app pins the exact tag and checks the SHA-256 of every file. It never uses `releases/latest`.

## Files — `supertonic3-int8-2026-05-11`

| File | Bytes | SHA-256 |
|---|---:|---|
| `duration_predictor.int8.onnx` | 3,700,147 | `c3eb91414d5ff8a7a239b7fe9e34e7e2bf8a8140d8375ffb14718b1c639325db` |
| `text_encoder.int8.onnx` | 36,416,150 | `c7befd5ea8c3119769e8a6c1486c4edc6a3bc8365c67621c881bbb774b9902ff` |
| `vector_estimator.int8.onnx` | 78,400,833 | `20cd86fa5c6effedfda0e7cffe5b0569ca401c440a0c3a1d72bf39286c0db3fd` |
| `vocoder.int8.onnx` | 25,991,073 | `e923d60f53f95eb1ce235f1dc33ec56d9c057823c96fa6f8acf98f32b0da6152` |
| `tts.json` | 8,253 | `42078d3aef1cd43ab43021f3c54f47d2d75ceb4e75f627f118890128b06a0d09` |
| `unicode_indexer.bin` | 262,144 | `8402ca48e5189a8950138580b0fff64db6f072f24ac07cd54ba8b2fbb9883b30` |
| **Total** | **144,778,600** | |

To verify, download the assets into one folder together with `SHA256SUMS` and run `sha256sum -c SHA256SUMS --ignore-missing`.

## Where the files come from

1. **Model**: Supertonic 3 by Supertone Inc. — <https://huggingface.co/Supertone/supertonic-3>. Supertone publishes fp32 ONNX files.
2. **These files**: int8 ONNX files distributed by the sherpa-onnx project (k2-fsa) in
   [`sherpa-onnx-supertonic-3-tts-int8-2026-05-11.tar.bz2`](https://github.com/k2-fsa/sherpa-onnx/releases/download/tts-models/sherpa-onnx-supertonic-3-tts-int8-2026-05-11.tar.bz2)
   (128,774,318 bytes · SHA-256 `82fa96f9…432c427`). We downloaded it on 2026-11-16. GitHub's digest for that asset matched on 2026-11-26.
3. The six files above were extracted from that bundle byte for byte. **We did not modify them.**
   They differ from Supertone's published files. See `NOTICE`.

## License

The model and the files derived from it are licensed under the **BigScience Open RAIL-M License** — see [`LICENSE`](LICENSE).
It is an unchanged copy of <https://huggingface.co/Supertone/supertonic-3/resolve/main/LICENSE>.

- **Use restrictions apply.** Paragraph 5 and Attachment A forbid certain uses. If you use or redistribute these files, you must follow them and pass them on to your users.
- **Attachment A (e)**: content generated with the model must be clearly disclosed as machine generated.
- The upstream bundle also contains an MIT `LICENSE`. It covers Supertone's sample code, **not** the model weights.
- This repository is not affiliated with or endorsed by Supertone Inc. or the sherpa-onnx project.

Copyright (c) 2026 Supertone Inc. — see `NOTICE` for the full attribution.

---

## 한국어 요약

**수수리드(SusuRead)** 앱의 온디바이스 AI 음성이 쓰는 모델 파일을 배포하는 저장소입니다. 앱이 이 저장소의 **Releases** 에서 파일을 내려받습니다. 음성은 기기 안에서 만들어지고, 책의 문장은 기기를 떠나지 않습니다.

- 코드는 없습니다. 모델 파일은 git 에 커밋하지 않고 Releases 에만 첨부합니다.
- release 는 **불변**입니다. 모델이 바뀌면 새 태그를 만들고, 옛 태그는 지우지 않습니다. 앱은 태그를 고정해서 받고, 파일마다 SHA-256 을 확인합니다.
- 출처: Supertone Inc. 의 Supertonic 3 → sherpa-onnx(k2-fsa)가 배포한 int8 묶음. 그 묶음에서 바이트 그대로 꺼냈고 **고치지 않았습니다.**
- 라이선스: **BigScience Open RAIL-M** (`LICENSE` — 원문 그대로). **사용 제한(5항 · 첨부 A)** 이 있습니다. 이 파일로 만든 음성은 **기계 생성임을 밝혀야** 합니다(첨부 A (e)). 묶음 안의 MIT 라이선스는 예제 코드의 것이고 모델의 것이 아닙니다.
- 이 저장소는 Supertone Inc. 나 sherpa-onnx 프로젝트와 관계가 없습니다.
