# Provenance — MinerU2.5-Pro-2605-1.2B

## Record status

- Record date: 2026-08-11; last updated: 2026-08-12
- Archive state: unpublished draft; independent review completed and required
  pre-publication corrections applied
- Planned release tag: `mineru2.5-pro-2605-1.2b-r1`
- Verification state: technical, integrity and legal checks passed; focused
  verification of the corrective changes remains required before publication

This record identifies the upstream artifact selected for the ToMD accurate
document-recognition component. The independent review result does not itself
publish the draft or authorize publication; only a separate decision by the
repository owner can do that.

## Upstream identity

- Publisher: OpenDataLab
- Model identifier: `opendatalab/MinerU2.5-Pro-2605-1.2B`
- Upstream repository: <https://huggingface.co/opendatalab/MinerU2.5-Pro-2605-1.2B>
- Pinned revision: `bff20d4ae2bf202df9f45284b4d43681555a97ed`
- Revision timestamp reported by upstream: `2026-06-16T05:59:05Z`
- ToMD component version: `2605-1.2b`
- Runtime component size: `2,328,010,562` bytes
- Largest source file: `model.safetensors`
- Largest source-file size: `2,312,126,640` bytes
- Largest source-file SHA-256: `abf8681ca63b8dec7b67de257af47b821f179442f72998d0696ae2ed9232a5f0`

The upstream API returned the exact requested revision as its `sha`; the model
was public, not gated and not disabled at the time of preparation. The pinned
revision, not the upstream default branch or a moving `latest` reference,
identifies the selected content.

## Upstream file inventory

The pinned revision contains thirteen files:

- `.gitattributes`
- `README.md`
- `added_tokens.json`
- `chat_template.jinja`
- `config.json`
- `generation_config.json`
- `merges.txt`
- `model.safetensors`
- `preprocessor_config.json`
- `special_tokens_map.json`
- `tokenizer.json`
- `tokenizer_config.json`
- `vocab.json`

The ToMD runtime component intentionally selects ten files. `.gitattributes` is
repository metadata. `README.md` is preserved separately as the release asset
`UPSTREAM-MODEL-CARD.md`. The standalone `chat_template.jinja` is not required
by the selected ToMD runtime and is excluded under the no downloaded-code and
no standalone interpreter-template boundary.

## License evidence

Both the exact-revision model card front matter and the exact-revision upstream
API metadata identify the license as Apache-2.0. The pinned revision contains no
separate `LICENSE` or `NOTICE` file.

The preserved upstream model-card snapshot is exactly `15,571` bytes with
SHA-256 `8f829b69be518375b02023f795b3898adec98f5ac37208239884ad88e9a21cb7`.

- SPDX identifier: `Apache-2.0`
- Official license text: <https://www.apache.org/licenses/LICENSE-2.0>
- Archive license copy: [`../LICENSE`](../LICENSE)
- Archive legal boundary: [`../LEGAL.md`](../LEGAL.md)
- Third-party notices: [`../legal/THIRD_PARTY_NOTICES.md`](../legal/THIRD_PARTY_NOTICES.md)

Copyright in the model assets remains with OpenDataLab and other applicable
upstream rightsholders. This archive does not claim authorship or exclusive
ownership of the model and does not claim affiliation or endorsement.

## Technical verification performed by preparer

The preparer downloaded the ten runtime files from URLs containing the full
pinned revision and verified all sizes and SHA-256 digests recorded in the
archive manifest. All eight JSON files parsed successfully.

`config.json` identifies `Qwen2VLForConditionalGeneration`, reports model type
`qwen2_vl` and contains no `auto_map`. The weight file has a valid SafeTensors
JSON header, metadata format `pt`, 681 tensors and only BF16 tensor data. No
Pickle or downloaded Python module is part of the component.

The weight file was split into 35 ordered transport parts. The first 34 parts
are `67,108,864` bytes each and the final part is `30,425,264` bytes.
Concatenating parts `aaa` through `abi` produced a file that passed both
byte-for-byte comparison and the expected source SHA-256 check.

The independent reviewer repeated the upstream, asset, reconstruction,
SafeTensors, security and legal checks and reported no mismatch. The review
covered all 49 draft assets and reconstructed the original weight file with the
expected size and SHA-256. The recorded result is linked below.

## Redistribution requirements

The first immutable release must satisfy all of the following conditions:

1. Every runtime source file is obtained from the pinned upstream revision.
2. Each source file is recorded with its exact path, byte size and SHA-256.
3. No executable, Python module, plugin or remote-code loader is included.
4. Runtime model data and declarative configuration are not modified.
5. Transport parts reconstruct the original file byte-for-byte.
6. The Apache-2.0 text, model-card snapshot and attribution are included.
7. Third-party names are used only for origin and compatibility identification.
8. The release tag and assets become immutable when published.
9. The signed ToMD application manifest, not a remote checksum, controls installation.

## Independent review and publication control

Independent review completed on 2026-08-12 with verdict `ACCEPT AFTER FIXES`.
The technical, integrity and legal verification passed. The required fixes were
to remove mutable lifecycle assertions from the immutable manifest, update the
publication text, make reconstruction fail closed and protect the planned tag.

Those corrections are now applied. The release must remain a draft until a
focused independent review confirms them and the repository owner separately
authorizes publication. The current publication state is determined by the
GitHub Release page, not by this provenance record.
