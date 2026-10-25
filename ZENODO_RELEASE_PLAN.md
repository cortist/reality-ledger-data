# Zenodo release preparation — Cortist Reality Ledger

**Status: Prepared for review. No Zenodo DOI or GitHub release has been created.**

Zenodo GitHub integration was enabled for `cortist/reality-ledger-data` on 25 October 2026. This setting alone is not a release; a GitHub release tag will trigger Zenodo's archiving workflow.

## Preserved data

- Dataset title: **Cortist Reality Ledger: Initial Public Evidence Snapshot**
- Release candidate: **v1.0**
- Snapshot date: **2026-10-25**
- Resource type for Zenodo: **Dataset** (rather than Software).
- Creator/corporate author for confirmation: **Cortist**.
- Original files: **10** immutable `snapshots/cl-0001-v1.json` through `cl-0010-v1.json`.
- Normalized derived export: `records.jsonl` with **10** cases and **12** distinct primary-source URLs.
- Provenance: `PROVENANCE.json` with SHA-256 checksums and the original Cortist deployment, `DATA_DICTIONARY.md`, `README.md`.
- Canonical record: https://cortist.com/reality-ledger/
- Hugging Face distribution: https://huggingface.co/datasets/cortist/reality-ledger

## HOLD: before publishing the first DOI

1. **Rights confirmation.** Confirm Cortist holds permission to license its original curation and original summaries. Linked third-party research is not included in any new Cortist license; do not imply ownership of linked sources.
2. **Choose the actual dataset reuse license**, documenting the choice and whether it applies to the original Cortist compilation only. Zenodo defaults to CC BY 4.0 if no license is supplied; never accept this default silently.
3. **Confirm author metadata.** The prospective creator entry is the project name `Cortist`. Confirm the name represents the rights holder/creator accurately before archiving; do not invent individual authors, ORCID IDs or institutional affiliations.
4. **Create a validated `.zenodo.json` in the repository root** after the decisions above. It should include `upload_type: "dataset"`, title, creators, English description, keywords, relevant links, a real release version, and the *approved* license.
5. **Check the release payload and link validity.** Validate all ten snapshots and source URLs, `records.jsonl`, archive checksums, page references and published version; preserve v1 originals.
6. Only then manually create a **GitHub Release** for tag `v1.0` on the main branch. Zenodo is expected to ingest the public release and mint a versioned DOI. Verify the actual Zenodo record, metadata, access rights, DOI and landing page before linking it elsewhere.
7. Future revisions must keep prior snapshots and issue subsequent versioned releases rather than silently replacing records.

## Suggested release summary

**Cortist Reality Ledger — Initial Public Evidence Snapshot (v1.0)**

> Public source-linked evidence register documenting ten consequential AI claims, primary-source references, explicit evidentiary limitations, and triggers for future reassessment. Contains ten preserved original JSON snapshots and a normalized JSONL research export. Source material belongs to its respective owners. This is a dated editorial evidence register, not ground-truth AI labeling or independently certified AI safety evaluation.

## Reference

- Zenodo GitHub integration: https://help.zenodo.org/docs/github/enable-repository/
- Metadata options: https://help.zenodo.org/docs/github/describe-software/zenodo-json/
- Zenodo licensing (default CC BY): https://help.zenodo.org/docs/deposit/describe-records/licenses/
