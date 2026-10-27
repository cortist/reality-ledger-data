# Hugging Face ↔ GitHub verification — 27 October 2026

**Dataset:** [cortist/reality-ledger](https://huggingface.co/datasets/cortist/reality-ledger)  
**Canonical publication:** [cortist/reality-ledger-data](https://github.com/cortist/reality-ledger-data)  
**Verification status:** **VERIFIED — CONTENT-EQUIVALENT**, not byte-identical  
**Dataset-card metadata status:** **VERIFIED — PUBLICLY UPDATED** (27 October 2026)  
**Verification date:** 2026-10-27

## Direct public readback

The public Hugging Face dataset API, tree listing, `README.md` and `records.jsonl` were successfully retrieved via a separate browser-rendering request path after earlier fetches failed. At verification, the public HF dataset commit was `1294768cdfbf5454828e05eda07bd2f7711d8b43` (last modified 2026-10-25T17:28:10Z); the published HF dataset card's SHA-256 was `c0b8dacc76d93ededd4e2400fd822cb1112ad10e95b1242c966f5cd947b49bd9`.

The public HF JSONL and GitHub's `records.jsonl` were parsed and compared **record by record**. For **all 10 IDs CL-0001 through CL-0010**:

- All fields common to both datasets (other than differently structured `sources` and `timeline`) matched.
- Every `snapshot_sha256` reference and version number matched.
- Every source name and original source URL matched in sequence.
- The structured Hugging Face timelines reconstructed exactly the GitHub timeline strings when normalized (including the multi-event entries for CL-0008 and CL-0010).
- There were no additional or missing case IDs.

**Important:** The JSONL files are intentionally **not byte-identical**. Hugging Face has extra interpretive metadata (`export_snapshot`, `interpretation_type`, `outcome_resolved`, `score`, `sources_count`) and structures source/event objects differently. The result is **content equivalence after explicit normalization**, not file-hash equality, a continuous sync mechanism, or an independent factual audit. A fresh verification is necessary following either publication's next change.

## Dataset-card metadata correction — now resolved

Following the owner-uploaded replacement of Hugging Face's `README.md`, the dataset was **re-read from the public Hugging Face HTTP endpoints** on 27 October 2026.

- The public `README.md` returned HTTP 200 and now contains the YAML entry `license: cc-by-4.0`.
- Hugging Face's dataset API independently reports `cardData.license = cc-by-4.0`.
- The public card includes the fixed-version Zenodo DOI **10.5281/zenodo.23650580** and explicitly distinguishes Cortist-licensed original material from linked third-party content.
- The obsolete claim “No open redistribution or commercial-use license has been selected or granted” is absent.
- New Hugging Face dataset revision: `ee8211eea398855c447aab3b4fec652568515f83`; last modified `2026-10-27T07:48:21Z`.
- The public HF `records.jsonl` returned HTTP 200 and contains **exactly ten records**, `CL-0001` through `CL-0010`. All ten `snapshot_sha256` values match GitHub's current `records.jsonl`; the earlier full source- and timeline-normalized content equivalence check remains documented above.
- The public file listing still includes the same `records.jsonl`, `exports/records.csv`, `metadata/source_manifest.json`, and `scripts/validate_dataset.py` resources. No dataset-record changes were requested or required.
- GitHub's immutable v1.0 source snapshots, its archived release, and the Zenodo DOI record were not altered.

**Resolved:** The specific metadata issue reported on 27 October 2026 is closed. Dataset-content synchronization is verified at this dated readback, but this is **not a permanently guaranteed live sync**, and later dataset changes require a fresh comparison.

Upload source: [`huggingface/README.md`](huggingface/README.md). Live destination: [HF dataset card](https://huggingface.co/datasets/cortist/reality-ledger).
