# Data dictionary and interpretation

## Source of truth

The immutable `snapshots/cl-XXXX-v1.json` files represent the original public Cortist Reality Ledger JSON snapshots dated **2026-10-25**. The normalized `records.jsonl` file is generated from those originals. Both are source-based editorial assessments, not independently certified ground-truth datasets.

## JSONL fields

| Field | Meaning |
| --- | --- |
| `id` | Stable case ID, e.g. `CL-0001`. |
| `version` | Public record snapshot version number; initially 1. |
| `record_url` | Canonical human-readable evidence page on Cortist. |
| `snapshot_url` | Public URL of the original dated JSON snapshot. |
| `source_date` | Original source baseline date, `YYYY-MM-DD` (not an exact time). |
| `snapshot_date` | Date this version was published, `YYYY-MM-DD` (not an exact time). |
| `topic` | Topic assigned by Cortist. |
| `state` | Cortist editorial category: `pending`, `announced`, or `documented`. Does **not** mean independently verified. |
| `status` | Narrow case-specific descriptive evidence status. |
| `organization` | Entities relevant to the claim. |
| `claim` | The precise question being tracked. |
| `evidence` | Brief summary of source-backed observations. |
| `limitations` | Boundary of what has and has not been established. |
| `next_evidence` | Specific trigger needed for a material reassessment. |
| `sources` | Array of source-label and absolute URL objects; optional source-specific `published` date only when present in the original. |
| `timeline` | Array of source-event strings preserving the original information, not additional inferred dates. |
| `news_url` | Linked Cortist explanatory article, if present. |
| `topic_url` | Linked topic hub on Cortist. |
| `snapshot_sha256` | SHA-256 of the original JSON snapshot bytes stored in `snapshots/`. |
| `original_schema_version` | Schema-version marker supplied by the original record. |

### Normalization notes

The first four v1 records encode `sources` as `[label, url]` pairs, while CL-0005 through CL-0010 encode them as objects. `records.jsonl` converts both to consistent objects without dropping original labels or URLs; the archival snapshot files retain original shapes.

Likewise `events` and `sourceTimeline` used different representations. The `timeline` export stores an array of source text strings; consult the original snapshots for their exact event/date structure.

**Date caution:** Date-only strings must not be interpreted as observations made at midnight. Some third-party viewers auto-convert them to midnight timestamps.

## Limitations and copyright

Not a comprehensive AI-claims corpus, randomized sample, outcome scorecard, safety certification, or independently validated benchmark. Neither the content of linked third-party works nor blanket rights to republish them are licensed by this repository. No `LICENSE` has yet been selected for Cortist-authored compilation material. See [README](README.md).
