# ToMD Model Archive

This public repository is a redistribution archive for model data used by the ToMD document conversion application.

## Current component

- Model: `opendatalab/MinerU2.5-Pro-2605-1.2B`
- Upstream publisher: OpenDataLab
- Upstream repository: https://huggingface.co/opendatalab/MinerU2.5-Pro-2605-1.2B
- Pinned upstream revision: `bff20d4ae2bf202df9f45284b4d43681555a97ed`
- Model license: Apache License 2.0
- Expected total component size: `2,328,010,562` bytes
- Archive status: no model release has been published yet

## Purpose

The archive provides a controlled fallback source for ToMD if the upstream model repository is temporarily unavailable or its download URLs change.

ToMD does not automatically trust files from this repository. Every downloaded file is checked against a manifest embedded in the signed application, including its expected path, exact size and SHA-256 digest.

## Licensing and attribution

Copyright in the model files remains with OpenDataLab and any other applicable upstream rightsholders.

The model files are redistributed under the Apache License 2.0 identified by the upstream model repository. Each model release will include the applicable license text and any upstream notice files supplied with the pinned revision.

The root `LICENSE` file applies to original metadata and documentation created specifically for this archive unless a file or release states otherwise. It does not replace or override the license attached to upstream model assets.

This repository is an unofficial redistribution mirror maintained for the ToMD application. ToMD is not affiliated with, sponsored by or endorsed by OpenDataLab.

## Integrity and packaging

Model content is not modified. A file that exceeds the GitHub Release per-asset size limit may be split into transport parts. ToMD will reconstruct the original file in temporary storage and verify the SHA-256 digest of both the parts and the reconstructed file before installation.

Published releases are immutable. Existing release assets are never replaced with a different model version. A new model or revision requires a new release identifier and a new application manifest.

The archive contains model data and declarative configuration only. It must not contain downloaded executable code, Python modules, plugins or remote-code loaders.

## Availability

GitHub Releases and the upstream repository are independent download sources. Neither source is treated as the authority for file integrity; the signed ToMD application manifest is authoritative.

After successful installation, the model is stored locally and ToMD document processing does not require either download source to remain online.
