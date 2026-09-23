# SEA-G2P Vietnamese native DLL — third-party notices

The Windows x64 `sea_g2p_native.dll` release asset is built from the pinned
[`pnnbao97/sea-g2p`](https://github.com/pnnbao97/sea-g2p/tree/ee2e80b0ac47f1d9403f5c5fd88ecd6265e4e6b1)
source at commit `ee2e80b0ac47f1d9403f5c5fd88ecd6265e4e6b1`. The upstream
project is Apache-2.0; its license text is attached as `Apache-2.0.txt`.

## Modification notice

This DLL is a modified build of the upstream SEA-G2P Rust core. The attached
`sea-g2p-rs-no-python.patch` makes PyO3 optional for the standalone build; the
external KokoroSharp fork adds a C ABI wrapper so the host can call the core
without Python. The DLL is built from that patched source and the wrapper.
This notice identifies those changes for Apache-2.0 redistribution purposes.

## Attributions and licenses

- Vietnamese Kokoro model and voicepack: ContextBoxAI (`iamdinhthuan`), under
  Apache-2.0 as declared by the pinned model card. The files are listed in
  [`KOKORO-EXPANSION-ASSETS.md`](../KOKORO-EXPANSION-ASSETS.md).
- SEA-G2P core and dictionary: Phạm Nguyễn Ngọc Bảo (`pnnbao97`), Apache-2.0.
- C ABI wrapper: the `sea-g2p-native` crate in the external KokoroSharp fork,
  declared MIT in its `Cargo.toml`; the project MIT license is attached as
  `KokoroSharp-MIT.txt`.

The native build's `Cargo.lock` pins these Rust packages. Their original
license/copyright files are bundled by package in
`SEA-G2P-third-party-licenses.zip`:

| Package | Version | License expression in package metadata |
| --- | --- | --- |
| aho-corasick | 1.1.5 | Unlicense OR MIT |
| bit-set | 0.5.3 | MIT OR Apache-2.0 |
| bit-vec | 0.6.3 | MIT OR Apache-2.0 |
| crossbeam-deque | 0.8.8 | MIT OR Apache-2.0 |
| crossbeam-epoch | 0.9.21 | MIT OR Apache-2.0 |
| crossbeam-utils | 0.8.23 | MIT OR Apache-2.0 |
| either | 1.18.0 | MIT OR Apache-2.0 |
| fancy-regex | 0.13.0 | MIT |
| libc | 0.2.189 | MIT OR Apache-2.0 |
| memchr | 2.8.3 | Unlicense OR MIT |
| memmap2 | 0.9.11 | MIT OR Apache-2.0 |
| once_cell | 1.21.4 | MIT OR Apache-2.0 |
| pyo3-build-config | 0.23.5 | MIT OR Apache-2.0 |
| rayon | 1.12.0 | MIT OR Apache-2.0 |
| rayon-core | 1.13.0 | MIT OR Apache-2.0 |
| regex | 1.13.1 | MIT OR Apache-2.0 |
| regex-automata | 0.4.18 | MIT OR Apache-2.0 |
| regex-syntax | 0.8.11 | MIT OR Apache-2.0 |
| target-lexicon | 0.12.16 | Apache-2.0 WITH LLVM-exception |
| tinyvec | 1.13.2 | Zlib OR Apache-2.0 OR MIT |
| tinyvec_macros | 0.1.1 | MIT OR Apache-2.0 OR Zlib |
| unicode-normalization | 0.1.25 | MIT OR Apache-2.0 |

The archive preserves the license files distributed with these pinned crate
sources. The lockfile can include optional or build-time crates; this list is
the complete locked package set, not a claim that every listed crate is linked
into the final DLL.
