# Cortist Reality Ledger — Research Dataset

**The future, held accountable.**

AI predictions. Industry promises. Scientific evidence. What actually happened.

[Official website](https://cortist.com/) · [Reality Ledger](https://cortist.com/reality-ledger/) · [Open Research & Data](https://cortist.com/open-research/) · [Hugging Face dataset](https://huggingface.co/datasets/cortist/reality-ledger)

## About this repository

This public repository preserves the **initial Cortist Reality Ledger evidence snapshot**, dated **25 October 2026**, for researchers, journalists and developers inspecting important AI claims against primary sources.

The snapshot contains **10 individually identified cases (CL-0001–CL-0010)**, with **12 distinct attributed primary-source URLs**. Each record distinguishes an original claim or question, what the cited source supports, known limitations, and what future evidence could materially change the assessment.

**Interpretation:** This is a versioned editorial evidence registry, **not independent ground-truth labeling, AI-system certification, a company ranking, a completed forecast-scoring exercise, or proof that an announced promise was fulfilled**.

## Files

| Path | Description |
| --- | --- |
| [`records.jsonl`](records.jsonl) | Normalized, newline-delimited JSON export of the 10 initial records. |
| [`snapshots/`](snapshots/) | Ten exact published `cl-XXXX-v1.json` source snapshots, preserved without field rewrites. |
| [`PROVENANCE.json`](PROVENANCE.json) | Original canonical snapshot URLs, per-file SHA-256 checksums, and export context. |
| [`DATA_DICTIONARY.md`](DATA_DICTIONARY.md) | Field definitions, source-link normalization, interpretation and rights notes. |
| [`LICENSE.md`](LICENSE.md) | CC BY 4.0 terms and explicit exclusion of third-party works. |
| [`.zenodo.json`](.zenodo.json) | Zenodo Dataset metadata for versioned DOI archiving. |

`records.jsonl` is a normalized derivative generated from the public Cortist v1 snapshots. **The original JSON snapshots are authoritative for their respective historical versions.** The Hugging Face publication is another discoverable dataset distribution and may be updated on a different schedule; do not assume byte-for-byte identity between platforms.

## Integrity and updating

- The case IDs and original snapshots must remain traceable. Revisions to substantive claims should create distinct `-v2.json`, `-v3.json` etc. snapshots rather than overwriting v1.
- `snapshot_sha256` in each normalized JSONL row is the SHA-256 of the corresponding *original snapshot JSON file*, not a hash of the normalized row.
- Primary sources are credited by name and original URL. A corporate announcement is not automatically independently corroborated evidence.
- This repository does not automatically synchronize with the live Cortist website or Hugging Face. Cross-publication requires checked, intentional commits.

## Provenance and responsible reuse

Original record pages and dated JSON files remain publicly accessible on [Cortist.com](https://cortist.com/reality-ledger/). Editorial descriptions are Cortist's analysis; external article content and linked research remain subject to their own copyright and terms.

**License: [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE.md) for original Cortist-owned content only.** Cortist's authored research compilation, source-linked summaries, normalization and documentation may be shared, adapted and commercially reused with proper attribution under that license. This permission **does not grant rights to third-party papers, articles, images, logos, software or other external content linked from the records**. Rights are described precisely in [LICENSE.md](LICENSE.md). Attribution should identify *Cortist*, the dataset version, the original URL and the license, and note modifications.

## Citation and DOI

Until a formally reviewed Zenodo release receives a DOI, cite the version and URL transparently, for example:

> Cortist (2026). *Reality Ledger: Initial Public Evidence Snapshot, v1.0 (25 October 2026).* GitHub: https://github.com/cortist/reality-ledger-data . Canonical record pages: https://cortist.com/reality-ledger/ .

**Zenodo connection is separate from publication:** The GitHub integration is enabled, and [Zenodo metadata](.zenodo.json) is prepared for the first release. **No Zenodo DOI has been minted yet.** Releasing a GitHub tag triggers Zenodo archiving; verify the actual Zenodo record and DOI before citing one. See [RELEASE_NOTES_v1.0.md](RELEASE_NOTES_v1.0.md) and the [release checklist](ZENODO_RELEASE_PLAN.md).

## Methodology and contact

- [Methodology](https://cortist.com/methodology/)
- [Editorial standards](https://cortist.com/editorial-standards/)
- [Contact Cortist](https://cortist.com/contact/)

*Cortist — Evidence over hype.*
