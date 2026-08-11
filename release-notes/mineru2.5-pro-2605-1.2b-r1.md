# MinerU2.5-Pro-2605-1.2B for ToMD — redistribution archive r1

> **Publication gate:** this release is a draft pending independent review. Do
> not publish it until the repository provenance record states that independent
> review passed and the repository owner separately authorizes publication.

This release is an unofficial redistribution archive of the ten runtime data
files selected by ToMD from OpenDataLab's
`opendatalab/MinerU2.5-Pro-2605-1.2B` revision
`bff20d4ae2bf202df9f45284b4d43681555a97ed`.

Upstream declares the model under Apache License 2.0. Copyright and other rights
remain with OpenDataLab and other applicable rightsholders. ToMD is not
affiliated with, sponsored by or endorsed by OpenDataLab or Hugging Face.

## Integrity

The authoritative source and transport metadata is
`mineru2.5-pro-2605-1.2b-r1.manifest.json`. Verify all downloaded payload assets
against `PAYLOAD-SHA256SUMS` before reconstruction.

Reconstruct the original weight file in the listed order:

```sh
cat model.safetensors.part-aa model.safetensors.part-ab model.safetensors.part-ac > model.safetensors
```

The reconstructed file must be exactly `2,312,126,640` bytes and have SHA-256:

```text
abf8681ca63b8dec7b67de257af47b821f179442f72998d0696ae2ed9232a5f0
```

Transport splitting does not modify the model. The source file is accepted only
after final reconstruction and verification.

## Legal and security boundary

The release includes the Apache-2.0 license, third-party notices and an
unmodified snapshot of the pinned upstream model card. It contains no
downloaded Python module, plugin, native executable or remote-code loader.

The signed manifest embedded in ToMD, not this remote release description or
remote manifest, is authoritative for installation.
