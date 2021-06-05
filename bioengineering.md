---
layout: page
permalink: /bioengineering/
title: Bioengineering
tags: [research, bioengineering, materials, compression, cauchy, blatz, biomechanical, finite, element]
modified: 01-05-2021
comments: false
---

_”Measuring devices capture infinitesimal units of time, the fastest and weakest movements, and the smallest variations of forces cannot escape them. They penetrate the intimate function of the organs where life seems to be translated by unceasing mobility.”_—Étiennes-Jules Marey

<br/>
<br/>
## Anatomical replicas
Anatomically realistic organ replicas provide more consistent results than the use of a living subject or cadaver. 
In the case of a kidney replica, the related work did neither deal with its design, nor its development using silicone as the only material.
To this end, I have designed a two step experimental pipeline: Uniaxial Compression (UC) testing and Cauchy stress modeling.
The pipeline revealed that none of the available manufacturer silicone brands are suitable for the task of creating a realistic kidney.
<details><summary><b>Read more</b></summary>
<p>
The main findings were: 
(1) the silicones advertised as corresponding to the target ranges of elastic properties of a human kidney do not fall within the required target compression moduli,
(2) the data we’ve shared showcases less variability and uncertainty (inc. low (E1) and high (E2) strain moduli), 
(3) the E(max) occurs at a much later stage, 
(4) the maximal reachable stress of the tested silicone mixtures is larger than literature-based reports, and
(5) the parameters characterizing the nonlinear elastic model of the silicone mixtures are made available for the purpose of nonlinear finite element simulation of an entire kidney. Altogether these results provide a reference for future work concerned by designing organ replicas.
</p><p>
All measured and curated data from the UC testing and the source code for the Cauchy stress modeling and technical validation are openly available at the <a href='https://archive.materialscloud.org/record/327'>Materials Cloud Archive</a>. A `<a href='https://bioengineeringcommunity.nature.com/posts/designing-anatomical-organ-replicas'>Behind the paper</a>’ post is published in <a href='https://bioengineeringcommunity.nature.com/channels/541-behind-the-paper'>Bioengineering</a>, a Nature Research Community section. 
</p>
</details>
<br/>
[![DOI](/images/id_nature.jpg)](https://www.nature.com/articles/s41598-020-68886-3)

<br/>
<br/>
## Biomechanical models

Soft tissue deformation severely impacts the registration of image-based models during computer-assisted navigation in laparoscopic liver surgery. 
However, quantifying the impact of different limiting factors on non-rigid volume-to-surface registration performance remains an open research question.
These limiting factors are: the target surface size, its orientation, and the mesh quality.
My objective was to provide solutions to mitigate and even counteract their effects.
To that end, I designed three experiments and a computational pipeline to evaluate each factor independently. 
The pipeline consisted of creating a biomechanical model by using the physics-based shape matching, solving the differential equations for the non-linear deformations using the finite element method, discretizing the deformed surface to a 1024<sup>3</sup> voxel grid to capture the deformations and to compute similarity, distance, and classical metrics.
<details><summary><b>Read more</b></summary>
<p>
Using the Hausdorff distance, I reported a statistical significance for the different partial surfaces used for registration. 
With the help of the evaluation pipeline and a sensitivity analysis, I found that removing non-manifold geometry and improving the mesh quality noise resulted in better registration performance.
Another important result is redefining the state of the art available surface size from 20 to 16.5% to successfully register the bioomechanical model.
The different strategies restricted the limiting factors and improved registration results. 
All reference data, models, and evaluation results are [openly available](https://github.com/ghattab/EvalPBSM/).
</p>
</details>
<br/>
[![DOI](/images/id_springer.png)](https://dx.doi.org/10.1007%2Fs11548-020-02123-0)
