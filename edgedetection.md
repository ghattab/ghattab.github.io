---
layout: page
permalink: /edgedetection/
title: Edge detection
tags: [research, image, processing, edge, detection, computer, vision]
modified: 03-06-2021
comments: false
---

_"A visual image is constructed by our brain's ability to group signals together in the form of edges."_

<br/>
<br/>
## Edge learning   
In robotic-assisted kidney surgery, computational methods make it possible to augment the surgical scene and potentially improve patient outcome.
[Soft-tissue registration](/bioengineering/#biomechanical-models) is a prerequisite for the visualization of tumors and vascular structures hidden beneath the surface. 
State-of-the-art volume-to-surface registration methods, however, are computationally demanding and require a sufficiently large target surface.
To overcome this limitation, the first step toward registration is the extraction of the outer edge of the kidney.
To tackle this task, I proposed a deep learning-based solution. Rather than working only on the raw laparoscopic images, the network is given depth information and distance fields to predict whether a pixel of the image belongs to an edge. 
I evaluated the method on expert-labeled *in vivo* data from the EndoVis sub-challenge 2017 Kidney Boundary Detection and define the current state of the art.
<details><summary><b>Read more</b></summary>
<p>
By using a leave-one-out cross-validation, I reported results for the most suitable network with a median precision-like, recall-like, and Intersection over Union (IoU) of 39.5 px, 143.3 px, and 0.3, respectively.
I concluded that this approached succeeded in predicting the edges of the kidney, except in instances where high occlusion occurs, which explains the average decrease in the IoU score.

</p>
</details>
<br/>
[![DOI](/images/id_springer.png)](https://doi.org/10.1007/s11548-019-02102-0)

<br/>
<br/>
## Edge quality
Object detection and image segmentation of regions of interest provide the foundation for numerous pipelines across disciplines. 
Robust and accurate computer vision methods are needed to properly solve image-based tasks. 
Multiple algorithms have been developed to solely detect edges in images.
Constrained to the problem of creating a thin, one-pixel wide, edge from a predicted object boundary, we require an algorithm that removes pixels while preserving the topology.
Thanks to skeletonize algorithms, an object boundary is transformed into an edge; contrasting uncertainty with exact positions. 
To extract edges from boundaries generated from different algorithms, I presented a computational pipeline that relies on:
a novel skeletonize algorithm,
a non-exhaustive discrete parameter search to find the optimal parameter combination of a specific post-processing pipeline,
and an extensive evaluation using three data sets from the medical and natural image domains (kidney boundaries, NYU-Depth V2, BSDS 500). 
While the skeletonize algorithm was compared to classical topological skeletons, the validity of the post-processing algorithm was evaluated by integrating the original post-processing methods from six different works.
<details><summary><b>Read more</b></summary>
<p>
Using the state of the art metrics, precision and recall based Signed Distance Error and the Intersection over Union bounding box, the results indicated that the SDE metric for these edges was improved up to 2.3 times.
This work provided guidance for parameter tuning and algorithm selection in the post-processing of predicted object boundaries.
</p>
</details>
<br/>
[![DOI](/images/id_bmc.png)]()
