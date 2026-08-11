# MinerU2.5-Pro-2605-1.2B for ToMD — redistribution archive r1

> **Verification:** independent technical, integrity and legal review completed
> on 2026-08-12. The required corrections were applied and independently
> verified with final verdict `ACCEPT`. Publication is a separate
> repository-owner action. The authoritative current publication state is the
> GitHub Release metadata.

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

From a directory containing all downloaded release assets, verify every payload
before reconstruction and fail if any expected part is missing or corrupted:

```zsh
set -euo pipefail
export LC_ALL=C
shasum -a 256 -c PAYLOAD-SHA256SUMS

parts=(model.safetensors.part-a??(N))
(( ${#parts[@]} == 35 ))
for part in "${parts[@]}"; do
  [[ -f "$part" ]]
done

cat "${parts[@]}" > model.safetensors
[[ "$(wc -c < model.safetensors | tr -d ' ')" == "2312126640" ]]
printf '%s  %s\n' \
  'abf8681ca63b8dec7b67de257af47b821f179442f72998d0696ae2ed9232a5f0' \
  'model.safetensors' | shasum -a 256 -c -
```

The reconstructed file must be exactly `2,312,126,640` bytes and have SHA-256:

```text
abf8681ca63b8dec7b67de257af47b821f179442f72998d0696ae2ed9232a5f0
```

The command names the exact manifest order `aaa` through `abi` and requires all
35 parts. Transport splitting does not modify the model. The source file is
accepted only after payload, final-size and final SHA-256 verification succeeds.

## Legal and security boundary

The release includes the Apache-2.0 license, third-party notices and an
unmodified snapshot of the pinned upstream model card. It contains no
downloaded Python module, plugin, native executable or remote-code loader.

The signed manifest embedded in ToMD, not this remote release description or
remote manifest, is authoritative for installation.
