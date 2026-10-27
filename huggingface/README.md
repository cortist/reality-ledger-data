---
pretty_name: Cortist Reality Ledger — AI Claims and Evidence
license: cc-by-4.0
language:
  - en
size_categories:
  - n<1K
tags:
  - artificial-intelligence
  - ai-safety
  - evidence
  - forecasting
  - source-attribution
  - ai-agents
  - research
configs:
  - config_name: default
    data_files:
      - split: train
        path: records.jsonl
---

<div align="center">

# CORTIST · REALITY LEDGER

**The future, held accountable.**

**AI predictions. Industry promises. Scientific evidence. What actually happened.**

[**Official website**](https://cortist.com) · [**Reality Ledger**](https://cortist.com/reality-ledger/) · [**What Changed?**](https://cortist.com/reality-ledger/changes/) · [**Evidence Watch**](https://cortist.com/reality-ledger/evidence-watch/) · [**GitHub**](https://github.com/cortist)

</div>

---

## License, source rights, and permanent citation

**License:** [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) applies to Cortist-authored editorial summaries, original structured compilation, source annotations, and documentation only, to the extent Cortist holds those rights. Commercial reuse of those licensed materials is permitted with attribution; linked third-party publications, papers, figures, images, code, logos, and trademarks remain under their respective rights and are **not** relicensed by Cortist. See the [scope-of-license statement](https://github.com/cortist/reality-ledger-data/blob/main/LICENSE.md).

**Archived initial dataset (version 1.0):** [Zenodo DOI **10.5281/zenodo.23650580**](https://doi.org/10.5281/zenodo.23650580). Recommended citation: Cortist (2026). *Cortist Reality Ledger: Initial Public Evidence Snapshot (v1.0)* [Data set]. Zenodo. https://doi.org/10.5281/zenodo.23650580.

This DOI identifies the fixed **25 October 2026** archived dataset version, not a guarantee that the continuing Hugging Face distribution is byte-identical to the GitHub JSONL export. The ten records refer to matching original Cortist snapshot hashes; Hugging Face additionally includes normalized source details and timeline structures. This card update is metadata-only and makes **no change** to the ten evidence records or the archived GitHub/Zenodo v1.0 release.

## Dataset summary

The **Cortist Reality Ledger** is a curated, source-linked registry of consequential AI claims, technical announcements, scientific findings, and questions that require future verification. Each row preserves an **original question**, the **documented evidence**, its **limitations**, a **next evidence trigger**, direct **source links**, and a reference to its dated public snapshot.

**This is a versioned editorial evidence registry, not a collection of independently verified ground-truth labels, a safety certification, or an AI-company ranking.** The data are intended for research discovery, source navigation and longitudinal documentation. They do not establish that any monitored promise has been fulfilled, nor that any unresolved claim has been independently validated.

| Release property | Value |
|---|---|
| Snapshot | **25 October 2026** |
| Export version | **1.0.0** |
| Records | **10** (`CL-0001` – `CL-0010`) |
| Original-source references | **12** |
| Public Ledger | [cortist.com/reality-ledger](https://cortist.com/reality-ledger/) |
| Dataset language | English |
| Source snapshots | Dated, individually addressable JSON files on Cortist |
| Independently scored Cortist forecasts | **0** at this release |

## Explore the records

Records span **AI safety**, **AI agents**, **AI and jobs**, **AI in medicine**, and **AI and energy**. Initial subjects include OpenAI/METR monitoring, MAI-DxO's retrospective results, Agent Compute Engine's announced preview, AISI's Mythos investigation, payroll indicators, junior hiring, agent sandboxes, training containment, grid rules and independent evaluator arrangements.

Open the [public index](https://cortist.com/data/reality-ledger/index.json) to see the canonical record references, or browse the [Ledger on Cortist](https://cortist.com/reality-ledger/).

## Repository contents

| File | Purpose |
|---|---|
| `records.jsonl` | **Canonical Hugging Face dataset**, one normalized public record per line. |
| `exports/records.csv` | Convenient tabular export; **not a separate data split**. |
| `metadata/source_manifest.json` | IDs, immutable source-snapshot URLs and SHA-256 hashes of their original JSON content. |
| `scripts/validate_dataset.py` | Offline structural validation and source-reference checks; does not independently confirm claims. |
| `CHANGELOG.md` | Export history and update policy. |

`records.jsonl` is the only configured dataset file in this card, avoiding duplicate counting of the CSV export. Hugging Face may label the technical split `train`; the rows **must not be treated as verified training labels**.

### Core fields

- `id`: stable claim identifier, such as `CL-0001`.
- `claim`: the specific question or statement under examination.
- `evidence`: Cortist's source-based summary at the export snapshot.
- `limitations`: what the evidence **does not** establish.
- `state`, `status`: descriptive evidence state, **not** a probability or verification score.
- `source_date`: date associated with the original cited source or finding.
- `snapshot_date`: date on which the historical Cortist record was published.
- `sources`: named external-source links, as a list of objects.
- `next_evidence`: what a meaningful future assessment would require.
- `timeline`: normalized list of source observations; these are **not** automatically post-publication status changes.
- `record_url`, `snapshot_url`, `snapshot_sha256`: provenance and source-file integrity.
- `outcome_resolved`, `score`: explicit **false/null** at this release.

All ten entries are editorial observations. `snapshot_sha256` hashes the unmodified source snapshot on Cortist; formatting and normalization make the exported JSONL row's hash different.

## How to load

```python
from datasets import load_dataset

dataset = load_dataset("cortist/reality-ledger", split="train")
print(dataset[0]["claim"])
print(dataset[0]["sources"])
```

Local equivalent:

```python
from datasets import load_dataset

dataset = load_dataset("json", data_files="records.jsonl", split="train")
```

The Hugging Face dataset ID above becomes usable **only after these files have actually been uploaded to a public dataset repository** under `cortist`.

## Collection and transformation

1. Original, publicly available Cortist ledger snapshot JSON files were read from the production file manifest current at export.
2. Record IDs (`CL-0001`–`CL-0010`), source links, dates, evidence summaries, limitations and follow-up triggers were preserved from those snapshots.
3. Two historical source schemas were mapped into a consistent JSONL schema. Earlier original-source pairs were normalized from `[name, URL]` to objects, without adding unsupported original publication dates.
4. Timelines were transformed into consistent lists of `{date, event, detail}`. Older event dates are retained as written; they are not asserted to be new revisions.
5. The exported rows include source JSON SHA-256 values for provenance checking.

**No external web pages, third-party articles, proprietary benchmark tables, or Metaculus forecast series are redistributed inside this dataset.** The `sources` values are attribution links, not copies of their content.

## Limitations and responsible use

- **Editorial interpretation:** Findings come from Cortist's public source-based assessments. A listed primary source can include a company statement rather than an independently reproduced finding.
- **No independent audit:** The collection itself has not undergone an independent external quality review. The ten cases have not been independently scored as predictions.
- **Small and selective:** Ten curated cases are not representative of all AI systems, all companies or all major announcements.
- **Snapshot, not live monitoring:** This export is frozen to 25 October 2026. Later changes must appear in subsequent versioned exports; this repository is **not** evidence that a continuous Hugging Face sync currently runs.
- **No automatic resolution:** A `documented`, `pending` or `announced` state should never be interpreted as a verified outcome or safety rating.
- **Source links may change:** Inspect the original publication and its current context before relying on individual conclusions.
- **Not for high-stakes decisions without external review:** Do not use as a sole basis for medical, employment, investment, security or regulatory decisions.

For corrections or follow-up evidence, see [Cortist's methodology](https://cortist.com/methodology/), the [What Changed?](https://cortist.com/reality-ledger/changes/) record, or [contact Cortist](https://cortist.com/contact/).

## License and provenance

**No open redistribution or commercial-use license has been selected or granted for this Hugging Face export.** Public access does not itself convey permission to republish Cortist's original commentary or commercialize it. Third-party sources and linked documents retain their respective owners' terms and rights. Contact [Cortist](https://cortist.com/contact/) to discuss licensing or professional data use.

For transparency and reproducibility, canonical snapshot links and content hashes are listed in [`metadata/source_manifest.json`](metadata/source_manifest.json). Links are not endorsements and should not be interpreted as independent verification.

## Citation

Suggested attribution if permitted by applicable rights:

> Cortist. (2026). *Cortist Reality Ledger: source-linked AI claims and evidence* (snapshot 2026-10-25, export v1.0.0). https://cortist.com/reality-ledger/

**Maintained by [Cortist](https://cortist.com). Evidence over hype.**
