---
layout: page
title: Peptide and Protein Molecular Encoder Data 2024
tags: [data, molecular encodings, encoder, fingerprint, machine learning, peptide classification]
modified: 09-08-2024
comments: false
---

The Peptide and Protein Molecular Encoder Data 2024 provides comprehensive data of peptides and proteins, including unnatural amino acids, for binary classification across various applications like antimicrobial and antiviral peptides, encoded using different fingerprints.
This dataset is essential for researchers in computational biology and bioinformatics.

## Peptide and Protein Molecular Encoder Data 2024

### Data Set Description

- **Type**: Fasta Files
- **Number of Instances**: Varies by dataset (incl. unbalanced classes)
- **Number of Variables**: Not applicable (sequence data)
- **Attribute Characteristics**: Categorical
- **Date Published**: 2024
- **Associated Tasks**: Binary classification

[Data](https://github.com/ghattab/iCAN/tree/main/Data/Original_datasets) are available for download under appropriate licensing. 

### Data Set Characteristics

| Characteristic               | Details                    |
|------------------------------|----------------------------|
| **Type**                     | Fasta Files                |
| **Number of Instances**      | Varies by dataset          |
| **Number of Variables**      | Not applicable             |
| **Attribute Characteristics**| Categorical |
| **Date Published**           | 2024                       |
| **Associated Tasks**         | Binary classification      |

### Data Sets 

The data sets consist of a total of 62 entries, each tailored to specific peptide prediction tasks across various domains. These data sets encompass a diverse range of applications, including anticancer, antimicrobial, and antiviral peptides.

## Overview of Domain Applications and Data Sets

| Domain                        | Explanation                                                                                                                   | No. data sets |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------|---------------|
| A-cell epitopes               | Prediction of peptides for modulating antigen presenting cells (modulating/non modulating).                                   | 1             |
| Anticancer peptides           | Prediction of peptides with cytotoxic efficiency against cancer cells (cytotoxic/non-cytotoxic).                             | 3             |
| Antifungal peptides           | Prediction of peptides with anti-fungal efficiency (anti-fungal/not anti-fungal).                                             | 2             |
| Anti-inflammatory peptides    | Prediction of therapeutic peptides against inflammatory diseases (anti-inflammatory/not anti-inflammatory).                   | 2             |
| Antimicrobial peptides        | Prediction of peptides with anti-microbial efficiency (antimicrobial/not anti-microbial).                                     | 7             |
| Amyloidogenic peptides        | Prediction whether peptides produce amyloid deposits, which may be deposited in organs or tissues under unnatural conditions. | 2             |
| Antitubercular peptides       | Prediction of peptides with anti-mycobacterial efficiency (antitubercular/not anti-tubercular).                               | 2             |
| Antiviral peptides            | Prediction of peptides with anti-viral efficiency (anti-viral/not anti-viral).                                                | 4             |
| Linear B-cell epitopes        | Prediction of B-cell epitopes (B-cell epitope/no B-cell epitope).                                                             | 1             |
| Cell-penetrating peptides     | Prediction of peptides with penetration capability of cell membranes (cell-penetrating/non cell-penetrating).                 | 10            |
| β-peptide foldamers           | Prediction whether peptides are β-amino acid oligomers and can adopt stable secondary structures.                             | 1             |
| Hemolytic peptides            | Prediction of peptides with hemolytic susceptibility (susceptible/resistant).                                                 | 1             |
| Human Immunodeficiency Virus  | Prediction with the HIV peptides show drug resistance to various drugs.                                                       | 17            |
| Immuno-suppressive peptides   | Prediction whether peptides reduce the activation or efficacy of the immune system.                                           | 1             |
| Neuro-peptides                | Prediction whether peptides are synthesized and released by neurons.                                                          | 1             |
| Permeability of cyclic peptides| Prediction of membrane permeability in cyclic peptides.                                                                      | 1             |
| Pro-inflammatory inducing peptides | Prediction whether peptides can increase inflammatory reaction as defense against pathogens.                            | 1             |
| Soluble *E.coli* proteins     | Prediction whether an *E.coli* protein is soluble or aggregation-prone.                                                       | 1             |
| Linear T-cell epitopes        | Prediction whether a peptide is an antigenic determinant, which is recognized by T-cells.                                     | 1             |
| Toxic peptides                | Prediction whether peptides are toxic.                                                                                        | 2             |
| Toxic proteins                | Prediction whether proteins are toxic.                                                                                        | 1             |


### Publications

Weckbecker, M., Anžel, A., Yang, Z., & Hattab, G. (2024). Interpretable molecular encodings and representations for machine learning tasks. Computational and Structural Biotechnology Journal.
https://doi.org/10.1016/j.csbj.2024.05.035

Hattab, G., Anžel, A., Spänig, S., Neumann, N., & Heider, D. (2023). A parametric approach for molecular encodings using multilevel atomic neighborhoods applied to peptide classification. NAR Genomics and Bioinformatics, 5(1), lqac103.
https://doi.org/10.1093/nargab/lqac103

Spänig, S., Mohsen, S., Hattab, G., Hauschild, A. C., & Heider, D. (2021). A large-scale comparative study on peptide encodings for biomedical classification. NAR genomics and bioinformatics, 3(2), lqab039.
https://doi.org/10.1093/nargab/lqab039

### Data Variables

- **Sequences**: Fasta files containing peptide and protein sequences, including unnatural and exotic amino acids.
- **Classes**: Binary classification labels for each sequence.

### Licensing

The data presented in this collection is built upon numerous datasets made available over time by other researchers, each accompanied by documented metadata, appropriate citations, and attributions to ensure proper credit and acknowledgment of the original sources.
