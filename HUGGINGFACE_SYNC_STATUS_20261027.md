# Hugging Face ↔ GitHub verification — 27 October 2026

**Dataset:** [cortist/reality-ledger](https://huggingface.co/datasets/cortist/reality-ledger)  
**Canonical publication:** [cortist/reality-ledger-data](https://github.com/cortist/reality-ledger-data)  
**Verification status:** **VERIFIED — CONTENT-EQUIVALENT**, not byte-identical  
**Dataset-card metadata status:** **PENDING HUGGING FACE UPLOAD**  
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

## Remaining issue: HF dataset card DOI and license

The live Hugging Face `README.md` **does not currently contain**:

- A YAML `license: cc-by-4.0` declaration;
- The version-specific Zenodo DOI **10.5281/zenodo.23650580**;
- Explicit attribution and the legal distinction between Cortist-owned CC-BY-4.0 material and third-party linked publications.

GitHub already has those details in `LICENSE.md`, `CITATION.cff`, and its main README.

The complete corrected **Hugging Face dataset card** is prepared in [`huggingface/README.md`](huggingface/README.md). It preserves the existing HF dataset documentation and adds only precise legal/citation metadata. **This prepared file has not been uploaded to Hugging Face.**

To complete the correction, an authorized owner/editor must replace **only HF's `README.md`** with the prepared content, then perform public readback of the updated YAML license and DOI. The safest one-off route is Hugging Face's authenticated web editor. For machine publishing, use an explicitly dataset-scoped fine-grained write token or appropriately configured trusted publishing; never post a token in a chat, store it in a public repo, use a broad-scope key, or mirror/delete unrelated HF files.

The GitHub `v1.0` release/tag, ten historical snapshots, Zenodo archive, and existing HF JSONL remain unchanged. No HF dataset-card upload or new Zenodo archive was performed by this verification.
