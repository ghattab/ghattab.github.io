---
layout: page
tags: [data, genomic islands, island, genome, genomics, machine learning, classification, horizontal gene transfer]
modified: 23-03-2026
comments: false
---

The Genomic Islands Detection Data 2025 provides a unified collection of datasets used for the detection of Genomic Islands (GIs). Genomic islands play a pivotal role in horizontal gene transfer (HGT), which is a primary driver of antimicrobial resistance (AMR) and bacterial evolution. This collection serves as a benchmark for researchers in computational biology and bioinformatics to develop and evaluate new detection methods.

## Genomic Islands Detection Data 2025
Source code, trained models, and the benchmark datasets are [available for download](https://github.com/andrejw27/genomic-data-representations-for-hgt-detection/tree/main/dataset/train_data) under appropriate licensing.

### Data Set Characteristics

| Characteristic | Detail |
| :--- | :--- |
| **Type** | FASTA Files |
| **Number of Instances** | Varies by sub-dataset |
| **Number of Variables** | Not applicable (Sequence-based) |
| **Attribute Characteristics** | Categorical |
| **Date Published** | 2025 |
| **Associated Tasks** | Binary classification (HGT vs. non-HGT) |

### Data Sets Description
Genomic segments acquired via HGT are known as **Genomic Islands (GIs)**. Each dataset within this collection consists of genomic segments classified as GIs (positive samples) or non-GIs (negative samples). 

- **Benbow**: Compiled by [Banerjee *et al.*](http://doi.org/10.1093/bioadv/vbae089), this is a unified, non-redundant dataset of 167 bacterial genomes.
- **IslandPick**: Originally constructed by [Langille *et al.*](http://doi.org/10.1186/1471-2105-9-329) (118 genomes) and later updated by [Bertelli *et al.*](http://doi.org/10.1093/bib/bby042) to include 104 bacterial genomes.
- **RVM**: Created by [Vernikos *et al.*](http://doi.org/10.1101/gr.7004508368), containing 32 species from the *Salmonella*, *Streptococcus*, and *Staphylococcus* genera.
- **GI-Cluster**: Evaluated by [Lu *et al.*](http://doi.org/10.1142/S0219720018400103), this dataset comprises 9 bacterial genomes based on comparative analysis by [Wei *et al.*](http://doi.org/10.1093/bib/bbw019372).
- **Literature**: A collection of 6 bacterial species with experimentally validated GIs as reported in [seminal literature](http://doi.org/10.1186/1471-2105-9-329).

### Overview of Data Sets

| Name | # Species | # Positive (GIs) | # Negative (non-GIs) |
| :--- | :---: | :---: | :---: |
| [**Benbow**](http://doi.org/10.1093/bioadv/vbae089) | 167 | 1,742 | 1,393 |
| [**IslandPick**](http://doi.org/10.1093/bib/bby042) | 104 | 1,845 | 3,266 |
| [**RVM**](http://doi.org/10.1101/gr.7004508368) | 32 | 331 | 337 |
| [**GI-Cluster**](http://doi.org/10.1142/S0219720018400103) | 9 | 625 | 1,743 |
| [**Literature**](http://doi.org/10.1186/1471-2105-9-329) | 6 | 80 | 182 |

### Publications

This dataset is associated with the following publications:

- Wijaya, A. J., Anžel, A., Richard, H., & Hattab, G. (2025). **Genomic data representations for horizontal gene transfer detection**. *NAR Genomics and Bioinformatics*, 7(4), lqaf165. [doi.org/10.1093/nargab/lqaf165](https://doi.org/10.1093/nargab/lqaf165)
- Wijaya, A. J., Anžel, A., Richard, H., & Hattab, G. (2025). **Current state and future prospects of horizontal gene transfer detection**. *NAR Genomics and Bioinformatics*, 7(1), lqaf005. [doi.org/10.1093/nargab/lqaf005](https://doi.org/10.1093/nargab/lqaf005)

### Data Variables

- **Sequences**: FASTA files containing the raw genomic segments.
- **Accession numbers**: Unique identifiers for the source sequences (NCBI/ENA).
- **Classes**: Binary labels (1 for GIs, 0 for non-GIs).

### Licensing

The data presented in this collection is built upon numerous datasets made available over time by other researchers, each accompanied by documented metadata, appropriate citations, and attributions to ensure proper credit and acknowledgment of the original sources.
