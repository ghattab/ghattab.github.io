---
layout: page
permalink: /bioimaging/
title: Bioimaging
tags: [research, bioimaging, biology, imaging, image, mining]
modified: 19-09-2019
comments: false
---

[<i class="fa fa-arrow-left"></i>](https://ghattab.github.io/research/)

<br/>
_"We may have knowledge of the past but cannot control it, we may control the future but have no knowledge of it."_―Claude E. Shannon

<br/>
<br/>
Understanding the mechanisms that regulate cellular reactions is facilitated by the coupling of high-resolution time-lapse imaging with microfluidic multiplexing.
These methods increase the rate at which microbiologists record cellular events and colony growth. Related work for computational analysis uses the general paradigm (i.e. segmentation, tracking, lineage construction).
However, none of the current approaches have been successful in extracting lineage information for *S. meliloti* colonies.
This bottleneck is attributed to high values for various data properties (cell number, cell shape diversity, noise, etc). Moreover, the large temporal separation between the images (i.e. the temporal resolution: 1 frame/30 min) is one of the biggest challenges in cell tracking. This hinders any possibility to segment and track individual cells.
<details><summary><b>Read more</b></summary>
<p>The task of characterizing different cell behaviors within a colony that are consistent in space and time corresponds to finding bacterial subpopulations. It is linked to many biological questions, such as bacterial pathogenesis or the study of metabolic interactions. I propose a novel framework that combines spatial and temporal coherence. It addresses the dynamics of rapid growth and the diversity of bacterial forms. The CYCASP framework examines (C)olon(Y) growth and (C)ell (A)ttributes in (SP)atiotemporal experiments by considering two new data abstractions: the particle and the patch.</p>
<p>
The main findings were: (1) the framework automatically processed both identification and tracking of bacterial subpopulations, (2) it selected groups of particle trajectories to obtain a better granularity of the colony growth, (3) the extracted patch lineages of different movies confirmed biological results from two separate experiments (e.g. quorum sensing), (4) a patch lineage is extracted in less than 5 min as opposed to 2 days of manual annotation for a given movie of 100 frames showcasing 300 cells.
</p><p>
Thanks to the particle abstraction, it is also possible to visualize a space-time cube of the particle trajectories at a rate of 1.15 s/frame. This software solution automatically creates a mental map of the colony and offers three different color mappings to highlight different features.
</p>
</details>
<br/>

[![DOI](//www.ncbi.nlm.nih.gov/corehtml/query/egifs/http:--www.frontiersin.org-alerts-logo-logo_LinkOut.jpg)](https://dx.doi.org/10.3389/fbioe.2018.00017) [![DOI](https://www.ncbi.nlm.nih.gov/corehtml/query/egifs/https:--academic.oup.com-images-oup_pubmed.png
)](https://academic.oup.com/bioinformatics/article-lookup/doi/10.1093/bioinformatics/bty889)
