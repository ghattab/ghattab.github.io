---
layout: page
tags: [data, open, syndrome, definition, machine learning, case definitions]
modified: 05-06-2026
comments: false
---

The Open Syndrome Case Definitions dataset is the first collection of public health case definitions available in both human-readable and machine-readable formats. It brings together 40 case definitions spanning a range of public health threats, countries, and health organizations, all structured under the Open Syndrome Definition (OSD) schema to support syndromic surveillance research and computational interoperability.

# Open Syndrome Case Definitions Data 2026

Source code, tools, and the dataset are freely available under the MIT license via [Hugging Face](https://huggingface.co/datasets/opensyndrome/case-definitions) and [GitHub](https://github.com/OpenSyndrome/definitions).


## Dataset Characteristics

| Characteristic | Detail |
|---|---|
| Type | JSON (machine-readable), PDF and TXT (human-readable) |
| Number of Instances | 40 case definitions |
| Number of Variables | ~21 fields per record (metadata + criteria groups) |
| Attribute Characteristics | Categorical and structured (nested inclusion criteria, logical operators, multi-organization, multi-threat) |
| Date Published | October 24, 2025 |
| License | MIT |
| DOI | `10.57967/hf/6635` |
| Schema Version | Open Syndrome Definition v1 (OSD v1) |
| Associated Tasks | Syndromic surveillance, interoperability research, AI-driven case classification, cross-jurisdictional comparison |
| Languages | English (primary); definitions sourced from multiple language contexts |


## Dataset Description

Case definitions are essential tools for public health practitioners: they are used to identify, monitor, and respond to diseases or groups of diseases. Despite their importance, no standardized, machine-readable format existed prior to this dataset, posing significant barriers to interoperability, computational processing, and AI-driven surveillance.

The collection comprises **36 national and regional definitions** representing 60 countries — including a regional block of 22 Pacific nations covered by the Pacific Public Health Surveillance Network (PPHSN) — and **4 continental or global definitions** from PAHO, ECDC, Africa CDC, and WHO. Five continents are covered: the Americas, Europe, Africa, Oceania, and Asia.

Each definition is available in three file formats following the naming convention `<public-health-threat>_<provenance-or-organization>`:

- **JSON** — structured under the Open Syndrome Definition (OSD v1) schema; machine-readable and JSON-LD compatible for semantic interoperability with ontologies such as HPO, MONDO, ICD, and SNOMED CT.
- **TXT** — extracted plain text of the case definition, one file per definition.
- **PDF** — original source documents from national and international health authorities.

File validation is enforced via automated GitHub Actions workflows, ensuring every JSON conforms to the OSD schema. All definitions were qualitatively reviewed for semantic fidelity between narrative and structured representations.

## Data Variables

The OSD format divides fields into two groups: **Metadata** (contextual provenance) and **Criteria** (structured clinical logic).

| Property | Group | Description |
|---|---|---|
| `title` | Metadata | Case definition title. |
| `description` | Metadata | Detailed description of the definition. |
| `scope` | Metadata | Level of specificity: `broad` or `specific`. |
| `category` | Metadata | Case classification: `confirmed`, `probable`, or `suspected`. |
| `version` | Metadata | Version of the case definition set by the author. |
| `open_syndrome_version` | Metadata | OSD schema version (currently `v1`). |
| `published_at` | Metadata | Publication date and time (UTC timestamp). |
| `published_in` | Metadata | Source or platform where the definition was published. |
| `location` | Metadata | Geographical location relevant to the definition's application. |
| `language` | Metadata | Language of the definition (e.g., English, Spanish). |
| `organization` | Metadata | Organization responsible for the definition. |
| `authors` | Metadata | List of authors of the case definition. |
| `keywords` | Metadata | Keywords related to the definition (e.g., COVID-19, mpox). |
| `target_public_health_threats` | Metadata | List of public health threats targeted by the definition. |
| `definition_type` | Metadata | Distinguishes *Case Definition* from *Syndromic Indicator*. |
| `status` | Metadata | Current state: `draft`, `published`, or `deprecated`. |
| `human_readable_definition` | Metadata | Plain-text summary for user interfaces. |
| `inclusion_criteria` | Criteria | Nested criteria (symptoms, diagnoses, lab tests, epidemiological links) combined via `AND`, `OR`, or `AT_LEAST` logical operators. Supports recursive nesting for complex decision trees. |
| `exclusion_criteria` | Criteria | Criteria that exclude a case from the definition; same structure as inclusion criteria. |
| `references` | Criteria | Scientific references supporting the definition (URL and title). |
| `notes` | Criteria | Additional remarks relevant to interpretation or use. |

## Accessing the Dataset

Two sources are available serving different needs: a frozen, citable bundle on Hugging Face, and a continuously updated repository on GitHub.

> **Which one should I use?** Use **Hugging Face** to reproduce or cite the paper exactly. Use **GitHub** when you want the freshest definitions for tooling and production.

**Hugging Face CLI (frozen bundle):**
```bash
pip install -U "huggingface_hub[cli]"
hf download opensyndrome/case-definitions \
  --repo-type dataset \
  --local-dir ./case-definitions
```

**Python:**
```python
from huggingface_hub import snapshot_download

path = snapshot_download(
    repo_id="opensyndrome/case-definitions",
    repo_type="dataset",
)
print(path)  # local cache directory containing all files
```

**Git:**
```bash
git lfs install
git clone https://huggingface.co/datasets/opensyndrome/case-definitions
```

**Single file by URL:**
```bash
curl -LO https://huggingface.co/datasets/opensyndrome/case-definitions/resolve/main/machine_readable/json/acuteflaccidparalysis_kenya.json
```

**GitHub (live definitions):**
```bash
git clone https://github.com/OpenSyndrome/definitions.git
```

The repository structure is:

```
.
├── human_readable/
│   ├── pdf/    # Original PDF source documents
│   └── txt/    # Extracted text, one file per definition
└── machine_readable/
    └── json/   # Open Syndrome Definition v1 JSON files
```

## Publications

This dataset is associated with the following publication:

Ferreira, A. P. G., Anžel, A., Marcilio, I., Hughes, H., Elliot, A. J., Kong, J. D., Schranz, M., Ullrich, A., & Hattab, G. (2025). *The Open Syndrome Definition as a Machine-Readable Standard for Public Health: Design and Implementation Study.* Journal of Medical Internet Research. Forthcoming. [doi.org/10.2196/86249](https://dx.doi.org/10.2196/86249) · [arXiv:2509.25434](https://arxiv.org/abs/2509.25434)


## Licensing

The dataset and all supporting tools are released under the MIT license. The definitions included in this collection are derived from official case definitions publicly shared by national and international health organizations. Each file is named to reflect its provenance, and the dataset includes documented metadata and attribution for each source to ensure proper credit to the originating authorities (WHO, ECDC, PAHO, Africa CDC, national ministries of health, and others).