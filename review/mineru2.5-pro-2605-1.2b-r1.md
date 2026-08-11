# Independent Review Procedure — MinerU2.5-Pro-2605-1.2B r1

This review must be performed by a person or agent that did not prepare the
draft release. The reviewer must inspect the actual repository commit, draft
release metadata and every uploaded asset; the preparer's report is not
sufficient evidence.

## Scope fixed for review

- Archive repository: `khascon/tomd-model-archive`
- Planned tag: `mineru2.5-pro-2605-1.2b-r1`
- Upstream model: `opendatalab/MinerU2.5-Pro-2605-1.2B`
- Upstream revision: `bff20d4ae2bf202df9f45284b4d43681555a97ed`
- Expected runtime source total: `2,328,010,562` bytes
- Expected draft payload assets: nine unchanged small runtime files and 35
  ordered parts of `model.safetensors`
- Expected total draft release assets: 49 (44 payload assets plus
  `LICENSE-Apache-2.0.txt`, `THIRD-PARTY-NOTICES.md`,
  `UPSTREAM-MODEL-CARD.md`, `PAYLOAD-SHA256SUMS` and the manifest)

## Required evidence

The independent review report must explicitly determine each of the following:

1. The upstream API resolves the full revision to the same commit and declares
   the model public, ungated and Apache-2.0.
2. The exact upstream tree contains no `NOTICE` or `LICENSE` file and the model
   card's acknowledgement and citation information is preserved.
3. The repository's `LICENSE`, `LEGAL.md`, third-party notices and provenance do
   not claim ownership, affiliation, endorsement or trademark rights in the
   upstream model.
4. The manifest contains exactly ten runtime source files and excludes the
   three non-runtime upstream files for the stated reasons.
5. Every small payload asset independently matches the pinned upstream file by
   byte size and SHA-256.
6. Every weight transport part matches its manifest size and SHA-256.
7. Concatenating exactly 35 parts from `aaa` through `abi` in manifest order
   produces exactly `2,312,126,640` bytes
   with SHA-256
   `abf8681ca63b8dec7b67de257af47b821f179442f72998d0696ae2ed9232a5f0`.
8. The reconstructed SafeTensors header is valid JSON and describes only tensor
   data expected by the component; no Pickle or executable payload is present.
9. Draft release assets contain no unexpected file, secret, credential,
   executable, Python module, plugin or symbolic link.
10. GitHub reports every draft asset upload as complete and its server-side
    digest, where exposed by the API, matches the local SHA-256.
11. The release is still a draft and release immutability is enabled for future
    publication.
12. The ToMD application repository and its signed embedded manifest were not
    modified by this archive-preparation stage.

## Decision rule

Any mismatch, missing legal evidence, unexplained file, incomplete upload or
inability to reconstruct the source weight file blocks publication. The review
report must distinguish confirmed defects from unresolved risks and must state
whether publication is approved or blocked.

Even an approving review does not publish the release. Publication requires a
separate authorization from the repository owner.

## Recorded independent review result

- Review completed: 2026-08-12
- Reviewer independence: the reviewer did not prepare the repository commit or
  draft Release
- Verdict: `ACCEPT AFTER FIXES`
- Technical, integrity and legal result: passed without mismatch across the
  pinned upstream revision, all 49 draft assets, reconstructed SafeTensors
  content and redistribution records
- Required corrections: remove mutable lifecycle state from the immutable
  manifest, replace the obsolete publication gate, protect the planned tag and
  tighten asset-count and reconstruction instructions
- Current status: corrections applied; focused independent verification and
  separate repository-owner authorization remain required before publication
