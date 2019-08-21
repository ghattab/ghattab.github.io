---
layout: page
permalink: /research/
title:
tags: [research]
modified: 02-07-2018
comments: false
---

[Last updated: 15-05-2019]


## Oncology: Translational surgery

Coming soon

## Bioimaging: Cell subpopulations

Understanding the mechanisms that regulate cellular reactions is facilitated by the coupling of high-resolution time-lapse imaging with microfluidic multiplexing.
These methods increase the rate at which microbiologists record cellular events and colony growth. Related work for computational analysis uses the general paradigm (i.e. segmentation, tracking, lineage construction).
However, none of the current approaches have been successful in extracting lineage information for *S. meliloti* colonies.
This bottleneck is attributed to high values for various data properties (cell number, cell shape diversity, noise, etc). Moreover, the large temporal separation between the images (i.e. the temporal resolution: 1 frame/30 min) is one of the biggest challenges in cell tracking. This hinders any possibility to segment and track individual cells.
[expand] The task of characterizing different cell behaviors within a colony that are consistent in space and time corresponds to finding bacterial subpopulations. It is linked to many biological questions, such as bacterial pathogenesis or the study of metabolic interactions. I propose a novel framework that combines spatial and temporal coherence. It addresses the dynamics of rapid growth and the diversity of bacterial forms. The CYCASP framework examines (C)olon(Y) growth and (C)ell (A)ttributes in (SP)atiotemporal experiments by considering two new data abstractions: the particle and the patch.[/expand]


[![DOI](//www.ncbi.nlm.nih.gov/corehtml/query/egifs/http:--www.frontiersin.org-alerts-logo-logo_LinkOut.jpg)](https://dx.doi.org/10.3389/fbioe.2018.00017)

The main findings were: (1) the framework automatically processed both identification and tracking of bacterial subpopulations, (2) it selected groups of particle trajectories to obtain a better granularity of the colony growth, (3) the extracted patch lineages of different movies confirmed biological results from two separate experiments (e.g. quorum sensing), (4) a patch lineage is extracted in less than 5 min as opposed to 2 days of manual annotation for a given movie of 100 frames showcasing 300 cells.
[expand] Thanks to the particle abstraction, it is also possible to visualize a space-time cube of the particle trajectories at a rate of 1.15 s/frame. This software solution automatically creates a mental map of the colony and offers three different color mappings to highlight different features. [/expand]


[![DOI](https://www.ncbi.nlm.nih.gov/corehtml/query/egifs/https:--academic.oup.com-images-oup_pubmed.png
)](https://academic.oup.com/bioinformatics/article-lookup/doi/10.1093/bioinformatics/bty889)


## Biophysics: Membrane proteins

The structural biology of membrane proteins (MP) is hampered by the difficulty in producing and purifying them. I conducted a comprehensive analysis of protein databases and a large scale analysis of expression protocols.
The former revealed that 213 unique membrane protein structures have been obtained after production of the target protein in *E. coli*. The latter consisted of text mining citing articles of each expression system. As found in the literature, there are three systems: primarily the T7 RNA polymerase, followed by the arabinose, then the T5 promoter based expression systems, respectively.
[expand] The main findings were: (1) the C41λ(DE3) and C43λ(DE3) bacterial mutant hosts have contributed to 28% of non *E. coli* MP structures, (2) there is a preference for a combination of bacterial host-vector together with a bimodal distribution of induction temperature and of inducer concentration. Altogether these analyses provide a set of rules for the optimal use of bacterial expression systems in MP production. Expression systems and bacterial hosts for MP structure determination are reported in the [Tool Box](http://www.ibpc.fr/UMR7099/tool_box/methodological_approaches.html) for MP studies. Detailed protocols to select bacterial expression mutant hosts and to optimize culture conditions are provided in Membrane Proteins Production for Structural Analysis. I. Mus-Veteau (Ed.), [Springer](https://link.springer.com/chapter/10.1007%2F978-1-4939-0662-8_4), NY, USA. [Chapter 4](http://www.ibpc.fr/UMR7099/Publis/pdf/Hattab14-2.pdf).[/expand]


[![DOI](//www.ncbi.nlm.nih.gov/corehtml/query/egifs/http:--www.nature.com-images-lo_npg.gif)](http://dx.doi.org/10.1038/srep12097)
