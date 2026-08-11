# Provenance — MinerU2.5-Pro-2605-1.2B

## Record status

- Record date: 2026-08-11
- Archive state: pre-publication
- Model assets published: no
- Verification state: pending preparation of the first immutable release

This record identifies the upstream artifact selected for the ToMD accurate document-recognition component. It does not claim that model files have already been mirrored or independently verified.

## Upstream identity

- Publisher: OpenDataLab
- Model identifier: `opendatalab/MinerU2.5-Pro-2605-1.2B`
- Upstream repository: https://huggingface.co/opendatalab/MinerU2.5-Pro-2605-1.2B
- Pinned revision: `bff20d4ae2bf202df9f45284b4d43681555a97ed`
- ToMD component version: `2605-1.2b`
- Expected total component size: `2,328,010,562` bytes
- Expected largest file: `model.safetensors`
- Expected largest-file size: `2,312,126,640` bytes

The pinned revision, not the upstream default branch or a moving `latest` reference, identifies the selected model content.

## License evidence

The upstream model repository identifies the model license as Apache License 2.0.

- SPDX identifier: `Apache-2.0`
- License text: https://www.apache.org/licenses/LICENSE-2.0
- Local archive license copy: [`../LICENSE`](../LICENSE)

Copyright in the model assets remains with OpenDataLab and any other applicable upstream rightsholders. This archive does not claim authorship or exclusive ownership of the model.

This is an unofficial redistribution mirror for the ToMD application. ToMD is not affiliated with, sponsored by or endorsed by OpenDataLab.

Before publication, the exact pinned revision must be checked for any additional copyright, attribution or notice files. Every applicable upstream notice must be preserved in the immutable release.

## Redistribution requirements

The first model release must satisfy all of the following conditions:

1. Every source file is obtained from the pinned upstream revision.
2. Each source file is recorded with its exact relative path, byte size and SHA-256 digest.
3. No executable code, Python module, plugin or remote-code loader is included.
4. Model data and declarative configuration are not modified.
5. A file split for transport is reconstructed byte-for-byte before its final SHA-256 verification.
6. The applicable license and upstream notice files are included with the release.
7. The release tag and assets become immutable when published.
8. ToMD treats its signed embedded manifest, not a remote checksum, as the authority for installation.

## Publication gate

Do not publish the model release until the archive manifest, transport parts, reconstructed output and legal notices have been independently checked against the pinned upstream revision.

When the verification is complete, this record must be updated before the immutable release is published. The final record must identify the release tag, archive manifest and verification result.
