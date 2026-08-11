# Legal and Distribution Boundaries

This document records the legal boundaries used to prepare the ToMD model
archive. It is a compliance record, not a legal opinion or a guarantee of
title. Material commercial distribution should still be reviewed by qualified
counsel for the distributor's jurisdiction and business model.

## Separate works and separate rights

This repository contains two legally distinct categories of material:

1. Original archive metadata and documentation prepared for ToMD. These files
   are licensed under the root Apache License 2.0 unless a file says otherwise.
   Copyright in that original material remains with the ToMD project author
   identified publicly by the GitHub account `khascon`.
2. Third-party model data originating from OpenDataLab's pinned Hugging Face
   revision. The upstream repository declares that model as Apache-2.0.
   Copyright and other rights in those assets remain with their applicable
   upstream rightsholders.

The ToMD application itself is not present in this repository. No access,
download, fork or redistribution of this archive grants a license to ToMD
application source code, binaries, product identity or branding except under a
separate license expressly supplied with those materials.

## Basis for redistribution

The exact upstream model page and API metadata for revision
`bff20d4ae2bf202df9f45284b4d43681555a97ed` identify the model license as
Apache-2.0. Apache License 2.0 permits reproduction and distribution, including
commercial distribution, subject to its conditions.

The archive applies those conditions conservatively:

- recipients are given the full Apache-2.0 license text;
- upstream origin and attribution are retained;
- no upstream runtime file is modified;
- transport splitting is disclosed and is reversed byte-for-byte;
- no upstream `NOTICE` file is omitted, because the pinned revision contains no
  file named `NOTICE` or `LICENSE`;
- the upstream model card is preserved as a release asset and remains available
  at its pinned upstream URL;
- no additional warranty or liability is accepted on behalf of OpenDataLab or
  any other contributor.

The absence of an upstream `NOTICE` file does not erase notices contained in
other source material. The upstream model card's acknowledgement and citation
information is therefore preserved by reference and by an unmodified snapshot
included with the release.

## Trademark and affiliation boundary

Apache License 2.0 does not grant trademark rights. `MinerU`, `OpenDataLab`,
`Hugging Face` and other third-party names are used only as reasonably necessary
to identify the source, compatibility and provenance of the component.

This archive is unofficial. ToMD and the archive maintainer are not affiliated
with, sponsored by, certified by or endorsed by OpenDataLab, Hugging Face or
other upstream projects. No third-party logo is included as ToMD branding.

## No silent substitution

The release tag, upstream revision, source hashes and transport hashes form one
fixed record. A changed upstream revision, corrected asset or different model
requires a new release identity and a new signed ToMD application manifest.
Published release assets must not be replaced in place.

The remote archive manifest is informative. It cannot authorize installation
or override the manifest embedded in a signed ToMD application. This prevents a
compromised hosting account from unilaterally changing trusted model content.

## Warranty, liability and operational risk

The Apache-2.0 warranty disclaimer and limitation of liability apply. The
archive maintainer does not promise continuous hosting, uninterrupted access,
accuracy of model output, fitness for a particular purpose, non-infringement or
compatibility with future ToMD versions.

GitHub may change service limits, suspend content or respond to legal process.
The existence of this archive is therefore a resilience measure, not a service
level guarantee. ToMD must fail closed if no source can provide assets matching
the signed application manifest.

## Publication gate

An immutable release may be published only after an independent reviewer has
verified the complete review checklist and the repository owner has separately
authorized publication. Discovery of conflicting ownership, licensing or
notice evidence blocks publication until resolved.
