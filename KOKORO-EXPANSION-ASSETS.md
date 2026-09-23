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

### Russian — zaakirio (Sveta, Masha, and Dima)

- Model source: [zaakirio/kokoro-ru at `d649c57b239b18c4c384378127cbf01dba039bc1`](https://huggingface.co/zaakirio/kokoro-ru/tree/d649c57b239b18c4c384378127cbf01dba039bc1). The upstream card identifies the weights as OpenRAIL and says the three voice actors consented to the Dialogs corpus release.
- Derivative-model license: [Dialogs OpenRAIL license at `e25ba617b2b56bd1dbf255d3905c51bd8da3d31f`](https://huggingface.co/datasets/langswap/dialogs-ru-emotional-conversations/blob/e25ba617b2b56bd1dbf255d3905c51bd8da3d31f/LICENSE.md). It expressly covers models trained on or derived from the corpus, permits redistribution including commercial use, and requires passing through its use restrictions. The exact license is attached as `Dialogs-OpenRAIL-LICENSE.md`.
- Base checkpoint: `hexgrad/Kokoro-82M`, Apache-2.0. RUAccent frontend assets are from [`ruaccent/accentuator` at `d7dee9e0261be2e2588830c8dd3810a9442db01c`](https://huggingface.co/ruaccent/accentuator/tree/d7dee9e0261be2e2588830c8dd3810a9442db01c), Apache-2.0.
- The six minimal eSpeak NG data files used by the Russian frontend are from the pinned Kokoro-Ru repository snapshot. They remain separately identified as GPL-3.0-or-later data; the upstream eSpeak NG `COPYING` text and source link are included. No eSpeak executable is mirrored here.
- Release files:
  - Model/config/voices: `kokoro-russian-zaakirio-base--onnx-model.onnx`, `kokoro-russian-zaakirio-dima--model-dima.onnx`, `kokoro-russian-zaakirio--config.json`, and `kokoro-russian-zaakirio--voices-{sveta,masha,dima}.bin`.
  - RUAccent: `kokoro-russian-ruaccent--dictionary-{accents,omographs,yo_homographs,yo_words}.json.gz`; `kokoro-russian-ruaccent--nn-accent-{config.json,model.onnx,vocab.txt}`; `kokoro-russian-ruaccent--nn-stress-{config.json,model.onnx,tokenizer.json}`; `kokoro-russian-ruaccent--nn-yo-{config.json,model.onnx,tokenizer.json}`; and `kokoro-russian-ruaccent--nn-omograph-{model.onnx,tokenizer.json}`.
  - eSpeak NG: `kokoro-russian-espeak--{phondata,phonindex,phontab,intonations,ru_dict}` and `kokoro-russian-espeak--lang-zle-ru`.
  - Notices: `Dialogs-OpenRAIL-LICENSE.md` and `eSpeak-NG-COPYING.txt`; the release's `NOTICE.md`, `KOKORO-EXPANSION-ASSETS.md`, and existing `Apache-2.0.txt` carry the remaining component notices.

## Not mirrored in this release

- **Turkish — Nisan:** the [source dataset](https://huggingface.co/datasets/omersaidd/tts_nisan_kumru_tur) carries MIT metadata, but its [open licensing discussion](https://huggingface.co/datasets/omersaidd/tts_nisan_kumru_tur/discussions/3) records the uploader saying it was assembled from videos found online, without resolving source permissions. The ONNX and voicepack encode that voice, so neither is mirrored until underlying recording/voice rights are clearer. The model's Apache-2.0/CC BY-SA 3.0 source terms allow broad use; this hold is about source provenance, not commercial-use or the mirror's business model.

This is a provenance record, not legal advice or a warranty that upstream rights are complete. Please review the linked pinned cards and license terms before use.
