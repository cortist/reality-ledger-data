# Zenodo v1.0 research dataset release — preparation status

**Repository metadata and license prepared. The actual GitHub Release / Zenodo DOI is not yet published.**

## Release identification

- GitHub repository: https://github.com/cortist/reality-ledger-data
- Zenodo integration: enabled for **this research repository only**, per Cortist Zenodo account settings (2026-10-25)
- Title: **Cortist Reality Ledger: Initial Public Evidence Snapshot (v1.0)**
- Creator: **Cortist** (project/organizational attribution)
- Type: **Dataset** (not software)
- Archived data date: **2026-10-25**
- Release/tag candidate: **v1.0**
- License: **Creative Commons Attribution 4.0 International (CC BY 4.0)** for Cortist-owned original dataset material only; third-party linked works are excluded
- Current DOI: **none — not yet registered**

## Integrity verified when preparing the repository

- Ten original `snapshots/cl-0001-v1.json` through `cl-0010-v1.json` files preserve their historical contents.
- The normalized `records.jsonl` includes ten unique cases and twelve distinct attributed HTTPS primary-source URLs.
- `PROVENANCE.json` records original immutable public snapshot URLs and SHA-256 hashes.
- `DATA_DICTIONARY.md` explains mixed original source structures, evidence boundaries, and date-only fields.
- `README.md` and `LICENSE.md` describe source attribution, rights, exclusions, and version history.

## What to check immediately before the first GitHub Release

1. Re-check `main` to ensure exactly the expected ten v1 snapshots, normalized export, provenance and valid Zenodo metadata exist. Do not overwrite v1 data; use new versioned files for substantive updates.
2. Verify that the Cortist project is authorized to license its *own* authored data, summaries and compilation under CC BY 4.0. This license cannot grant rights in linked third-party works.
3. Confirm metadata in `.zenodo.json`: `upload_type: dataset`, `version: 1.0`, `creators: Cortist`, `access_right: open`, `license: cc-by-4.0`.
4. Create **one** GitHub release from `main` using tag **`v1.0`**, title in `.zenodo.json`, and the publication summary in [RELEASE_NOTES_v1.0.md](RELEASE_NOTES_v1.0.md). Do not create extra releases or tags as tests.
5. Confirm Zenodo ingests **the actual GitHub release** (enablement alone does not generate a DOI). Inspect the Zenodo landing page for **Dataset** type, attribution, selected license, files and actual minted DOI.
6. Only after confirmation, add the DOI to GitHub README / Hugging Face / Cortist.com. The DOI must never be guessed.

## Future strategy

The public initial snapshot supports citation, discovery and reproducibility. Cortist's differentiated business offerings can focus on ongoing source monitoring, material-change alerts, premium longitudinal analysis and tailored B2B research. Openly licensed v1 material stays reusable under CC BY 4.0; later separate products need not be covered by this specific release.

## Official references

- [Zenodo .zenodo.json metadata](https://help.zenodo.org/docs/github/describe-software/zenodo-json/)
- [Zenodo GitHub repository enablement](https://help.zenodo.org/docs/github/enable-repository/)
- [Zenodo licenses and rights](https://help.zenodo.org/docs/deposit/describe-records/licenses/)
- [Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/)
