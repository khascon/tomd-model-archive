# ToMD Model Archive

This public repository is a redistribution archive for model data used by the
ToMD document conversion application. It is maintained independently from the
upstream model publisher.

## Current component

- Model: `opendatalab/MinerU2.5-Pro-2605-1.2B`
- Upstream publisher: OpenDataLab
- Upstream repository: <https://huggingface.co/opendatalab/MinerU2.5-Pro-2605-1.2B>
- Pinned upstream revision: `bff20d4ae2bf202df9f45284b4d43681555a97ed`
- Model license declared by upstream: Apache License 2.0
- Runtime component size: `2,328,010,562` bytes
- Planned release tag: `mineru2.5-pro-2605-1.2b-r1`
- Publication status: draft preparation; no immutable public model release yet

The exact file list, byte sizes, SHA-256 digests and transport mapping are in
[`manifests/mineru2.5-pro-2605-1.2b-r1.json`](manifests/mineru2.5-pro-2605-1.2b-r1.json).

## Purpose

This archive provides a vendor-controlled fallback source for ToMD if the
upstream model repository is unavailable or its URLs change. It is not a moving
mirror: every release identifies one immutable upstream revision.

ToMD must not automatically trust files merely because they are hosted here.
The signed ToMD application contains the authoritative installation manifest.
Every downloaded asset is checked against that manifest by expected name, byte
size and SHA-256 digest before it can be installed.

## Component boundary

The release contains only the ten runtime data and declarative configuration
files selected for ToMD. It does not contain downloaded Python modules,
plugins, native executables or a remote-code loader. The standalone upstream
`chat_template.jinja` is not part of the ToMD runtime component.

`model.safetensors` is larger than GitHub's per-asset limit. It is therefore
transported as three ordered byte ranges. Splitting is packaging only: the
reconstructed file must be verified as exactly `2,312,126,640` bytes with
SHA-256 `abf8681ca63b8dec7b67de257af47b821f179442f72998d0696ae2ed9232a5f0`
before installation.

## Licensing and rights

The upstream model repository declares the model as Apache-2.0. Copyright and
other rights in the model assets remain with OpenDataLab and any other
applicable upstream rightsholders. The archive does not relicense the model or
claim ownership of it.

The root [`LICENSE`](LICENSE) applies to original archive metadata and
documentation and supplies the Apache-2.0 text accompanying redistribution of
the model. Additional attribution and boundary statements are in:

- [`LEGAL.md`](LEGAL.md)
- [`legal/THIRD_PARTY_NOTICES.md`](legal/THIRD_PARTY_NOTICES.md)
- [`provenance/mineru2.5-pro-2605-1.2b.md`](provenance/mineru2.5-pro-2605-1.2b.md)

The ToMD application is a separate work and is not distributed from this
repository. Access to this archive grants no license to ToMD source code,
binaries, branding or other original ToMD materials except where their own
license expressly says otherwise.

`MinerU`, `OpenDataLab` and other third-party names are used only to identify
the origin of the redistributed component. This is an unofficial mirror. ToMD
is not affiliated with, sponsored by or endorsed by OpenDataLab.

## Publication controls

The first release must remain a GitHub draft until a reviewer who did not
prepare it independently verifies:

1. the upstream identity and Apache-2.0 license evidence;
2. every source-file size and SHA-256 digest;
3. every transport-part size and SHA-256 digest;
4. byte-for-byte reconstruction of `model.safetensors`;
5. the absence of executable code and unexpected files;
6. inclusion of the license, attribution and provenance records.

The review procedure is documented in
[`review/mineru2.5-pro-2605-1.2b-r1.md`](review/mineru2.5-pro-2605-1.2b-r1.md).
Publication requires a separate decision after that review. Once published,
the release and its assets are immutable and must never be silently replaced.

## Availability and warranty

GitHub Releases and the upstream repository are independent download sources;
neither is guaranteed to remain available. After a verified installation, ToMD
stores the component locally and document processing does not require either
source to stay online.

The component and archive metadata are supplied under the warranty and
liability limitations in Apache License 2.0. Nothing in this repository is a
promise of continuous hosting, model fitness, non-infringement or legal advice.
