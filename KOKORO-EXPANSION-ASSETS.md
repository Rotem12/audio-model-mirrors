# Kokoro language-expansion assets

Release tag: `kokoro-expansion-2026-09-23`

These files are re-hosted for the external KokoroSharp expansion work. They are not production catalog entries or a production approval. Each model's own license and upstream terms apply; the source cards are linked below at their pinned revisions. No expected byte sizes or checksums are recorded here.

## Included

### Arabic — Nabra

- Source: [marwanelamami/Nabra-82M-v0.1-ONNX at `85065b0be8573aefb401f8f53e7edc37d6556186`](https://huggingface.co/marwanelamami/Nabra-82M-v0.1-ONNX/tree/85065b0be8573aefb401f8f53e7edc37d6556186)
- Upstream card declares Apache-2.0, following the base model.
- Release files: `kokoro-arabic-nabra--nabra_fp32.onnx`, `kokoro-arabic-nabra--vocab.json`, `kokoro-arabic-nabra--voices_af_msa.pt`.

### German — Crane

- Source: [crane-local-ai/Kokoro-82M-v1.0-German-ONNX at `eeccb15741604cdc894053e1f4c72bb56c1a59be`](https://huggingface.co/crane-local-ai/Kokoro-82M-v1.0-German-ONNX/tree/eeccb15741604cdc894053e1f4c72bb56c1a59be)
- Upstream card declares Apache-2.0. It identifies Kerstin 1.0, the reference voice dataset, as CC0-1.0.
- Release files: `kokoro-german-crane--onnx-model.onnx`, `kokoro-german-crane--tokenizer.json`, `kokoro-german-crane--config.json`, `kokoro-german-crane--voices-df_kerstin.bin`.

### German — Martin

- Source: [Godelaune/Kokoro-82M-ONNX-German-Martin at `a1cba7fbf0e72fbae38f0a3a48ce0dc8e6077804`](https://huggingface.co/Godelaune/Kokoro-82M-ONNX-German-Martin/tree/a1cba7fbf0e72fbae38f0a3a48ce0dc8e6077804)
- Upstream card declares Apache-2.0 and asks users to credit the original authors and source model.
- Release files: `kokoro-german-martin--kokoro-martin.onnx`, `kokoro-german-martin--voices-martin.npz`.

### Marathi — Vivek

- Source: [shreyask/bol-tts-marathi-onnx at `985c7c42652bc9353598cc7ea8e086512bb04643`](https://huggingface.co/shreyask/bol-tts-marathi-onnx/tree/985c7c42652bc9353598cc7ea8e086512bb04643)
- Upstream ONNX card declares Apache-2.0 and links to the base model card for full citations. That card identifies Rasa and IndicVoices-R data under CC BY 4.0 and SPRINGLab/IndicTTS-Marathi under an IITM EULA. This mirror contains model artifacts, not those datasets; see the upstream card for the complete source-level attribution.
- Release files: `bol-tts-marathi-fp32--onnx-model.onnx`, `bol-tts-marathi-fp32--config.json`, `bol-tts-marathi-fp32--voices-mm_vivek.pt`.

### Swedish — Joakim

- Source: [Joakim/kokoro-sv-g2p at `a5aac876ccb2bf7480a129774c7e89cf3bbeac01`](https://huggingface.co/Joakim/kokoro-sv-g2p/tree/a5aac876ccb2bf7480a129774c7e89cf3bbeac01)
- Upstream card declares Apache-2.0; it says the reference voice derives from a public-domain LibriVox recording.
- Release files: `kokoro-swedish-joakim--kokoro_sv.onnx`, `kokoro-swedish-joakim--config.json`, `kokoro-swedish-joakim--sv_female.pt`.

### Vietnamese — ContextBoxAI model and SEA-G2P dictionary

- Model source: [contextboxai/Kokoro-Vietnamese at `9f210d622209fcc216fe2ac6159fed2ff381cb8a`](https://huggingface.co/contextboxai/Kokoro-Vietnamese/tree/9f210d622209fcc216fe2ac6159fed2ff381cb8a); upstream card declares Apache-2.0.
- Dictionary source: [pnnbao97/sea-g2p at `ee2e80b0ac47f1d9403f5c5fd88ecd6265e4e6b1`](https://github.com/pnnbao97/sea-g2p/tree/ee2e80b0ac47f1d9403f5c5fd88ecd6265e4e6b1); the pinned source is Apache-2.0.
- The Windows x64 native DLL is built from the pinned SEA-G2P source using the external fork's C ABI wrapper. The build patch and full Rust dependency license/copyright bundle accompany the DLL; see [`LICENSES/SEA-G2P-THIRD-PARTY-NOTICES.md`](LICENSES/SEA-G2P-THIRD-PARTY-NOTICES.md).
- Release files: `kokoro-vietnamese-contextbox--kokoro_vi.onnx`, `kokoro-vietnamese-contextbox--config.json`, `kokoro-vietnamese-contextbox--kokoro_vi_voicepack.pt`, `kokoro-vietnamese-contextbox--sea_g2p.bin`, `kokoro-vietnamese-contextbox--sea_g2p_native.dll`, `sea-g2p-rs-no-python.patch`, `SEA-G2P-third-party-licenses.zip`, and `KokoroSharp-MIT.txt`.

## Not mirrored in this release

- **Turkish — Nisan:** the pinned ONNX repository card describes CC BY-SA 3.0 training data but does not clearly state the separate license for the exported model and voice artifact. The model/voice files are withheld until those artifact rights are clear.
- **Russian — zaakirio:** the pinned card identifies a generic OpenRAIL family but supplies no exact license text; its package also includes eSpeak data identified as GPL-3.0-or-later. The Russian model and eSpeak files are withheld pending resolution of both terms.

This is a provenance record, not legal advice or a warranty that upstream rights are complete. Please review the linked pinned cards and license terms before use.
