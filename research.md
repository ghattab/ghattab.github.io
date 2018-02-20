---
layout: page
permalink: /research/
title: 
tags: [research]
modified: 11-10-2018
comments: false
---

[Last updated: 17-02-2018]


### Inquire Infer Innovate

## Bioimaging: Cell subpopulations

Understanding the mechanisms that regulate cellular reactions is facilitated by the coupling of high-resolution time-lapse imaging with microfluidic multiplexing.
These methods increase the rate at which microbiologists record cellular events and colony growth for different bacterial species (e.g. *Sinorhizobium meliloti*). However, this leads to a bottleneck in the analysis steps. Related work for computational analysis uses the general paradigm (i. e. segmentation, tracking, lineage construction).
However, none of the current approaches have been successful in extracting lineage information.
The inability to process this data was attributed to high values for various data properties: Cell number, cell shape diversity, cell density, noise and lateral resolution (60 nm/px). Furthermore, the large temporal separation between the images (i. e. the temporal resolution: 1 frame/30 min) is one of the biggest challenges in cell tracking. 
My primary goal is to characterize different cell behaviors within a colony that are consistent in space and time (i. e. coherent subpopulations). As a task, the search for bacterial subpopulations is linked to many biological questions, such as bacterial pathogenesis (David, 2013) or the study of metabolic interactions (Rosenthal et al., 2017). Due to the high values for the  five properties and the low temporal resolution, it is not possible to segment and track individual cells.
In order to overcome the bottleneck of the analysis, I propose a novel framework, an alternative to the single-celled paradigm that combines spatial and temporal coherence. The CYCASP framework examines (C)olon (Y) growth and (C)ell (A)ttributes in (SP)atiotemporal Experiments (CYCASP) and considers two new data abstractions to address the dynamics of rapid growth and the diversity of bacterial forms: the *particle* and the *patch*.
CYCASP selects groups of particle trajectories in order to obtain a better granularity of the colony’s growth. It allows us to process both identifcation and tracking of bacterial subpopulations. Contrary to a minimum of 2 days of manual analyses previously required of our collaborators, our reference results show that CYCASP can automatically extract patch lineages in less than 5 min for biological data sets of more than 100 frames and 300 cells.

[![DOI](//www.ncbi.nlm.nih.gov/corehtml/query/egifs/http:--www.frontiersin.org-alerts-logo-logo_LinkOut.jpg)](http://dx.doi.org/10.1038/srep12097)


## Biophysics: Membrane proteins

The structural biology of membrane proteins (MP) is hampered by the difficulty in producing and purifying them. I conducted a comprehensive analysis of protein databases and a large scale analysis of expression protocols.
The former revealed that 213 unique membrane protein structures have been obtained after production of the target protein in *E. coli*. The latter consisted of text mining citing articles of each expression system. As found in the literature, there are three systems: primarily the T7 RNA polymerase, followed by the arabinose, then the T5 promoter based expression systems, respectively. 
The main findings were: (1) the C41λ(DE3) and C43λ(DE3) bacterial mutant hosts have contributed to 28% of non *E. coli* MP structures, (2) there is a preference for a combination of bacterial host-vector together with a bimodal distribution of induction temperature and of inducer concentration. 
Altogether our analyses provide a set of rules for the optimal use of bacterial expression systems in MP production.


[![DOI](//www.ncbi.nlm.nih.gov/corehtml/query/egifs/http:--www.nature.com-images-lo_npg.gif)](http://dx.doi.org/10.1038/srep12097)


Expression systems and bacterial hosts for MP structure determination are reported in the [Tool Box](http://www.ibpc.fr/UMR7099/tool_box/methodological_approaches.html) for MP studies. Detailed protocols to select bacterial expression mutant hosts and to optimize culture conditions are provided in Membrane Proteins Production for Structural Analysis. I. Mus-Veteau (Ed.), [Springer](https://link.springer.com/chapter/10.1007%2F978-1-4939-0662-8_4), NY, USA. [Chapter 4](http://www.ibpc.fr/UMR7099/Publis/pdf/Hattab14-2.pdf).
