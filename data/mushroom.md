---
layout: page
title: The Mushroom Data Set 2020
tags: [data, UCI, mushroom, edible, poisonous, simulation, classification]
modified: 09-08-2024
comments: false
---

The Mushroom Data Set 2020 provides a comprehensive overview of mushroom species, focusing on their physical characteristics and classification as either poisonous or edible. 

## Mushroom Data Set 2020

### Data Set Description

- **Primary Data**: Describes 173 mushroom species, used for simulating hypothetical mushrooms.
- **Secondary Data**: Contains 61,069 hypothetical mushrooms for binary classification.

[Source code and data](https://github.com/ghattab/secondarydata) are available for download under CC BY 4.0 Licensing. 

### Data Set Characteristics

| Characteristic               | Details                    |
|------------------------------|----------------------------|
| **Type**                     | Multivariate               |
| **Number of Instances**      | 173 (Primary), 61,069 (Secondary) |
| **Number of Variables**      | 20                         |
| **Attribute Characteristics**| Qualitative and Quantitative |
| **Date Published**           | 15.10.2020                |
| **Missing Values**           | Yes (Primary), No (Secondary) |

### Primary Data Set Characteristics

| Characteristic               | Details                    |
|------------------------------|----------------------------|
| **Type**                     | Multivariate               |
| **Number of Instances**      | 173                        |
| **Number of Variables**      | 20                         |
| **Attribute Characteristics**| Qualitative and Quantitative |
| **Date Published**           | 15.10.2020                 |
| **Associated Tasks**         | Data simulation            |
| **Missing Values**           | Yes                        |
| **Metadata Download**        | [Download Metadata](#)     |

### Secondary Data Set Characteristics

| Characteristic               | Details                    |
|------------------------------|----------------------------|
| **Type**                     | Multivariate               |
| **Number of Instances**      | 61,069                     |
| **Number of Variables**      | 20                         |
| **Attribute Characteristics**| Qualitative and Quantitative |
| **Date Published**           | 15.10.2020                 |
| **Associated Tasks**         | Binary classification      |
| **Missing Values**           | No                         |
| **Metadata Download**        | [Download Metadata](#)     |

### Comparison with UCI 1987

The Mushroom Data Set 2020 provides a modernized approach to mushroom classification, building on the foundational UCI 1987 data set. While the UCI 1987 dataset focused on a limited number of species with predefined attributes, the 2020 dataset expands significantly in terms of species diversity and number of hypothetical instances. This expansion allows for more robust machine learning applications and provides a comprehensive testbed for binary classification tasks. For more details, please see the [Results section of the publication] (https://www.nature.com/articles/s41598-021-87602-3#Sec2).

### Citation

Wagner, D., Heider, D., & Hattab, G. (2021). Mushroom data creation, curation, and simulation to support classification tasks. *Scientific Reports*, 11, 8134. [DOI:10.1038/s41598-021-87602-3](https://doi.org/10.1038/s41598-021-87602-3)

### Data Variables

| Variable                    | Measurement  | Values                                   |
|-----------------------------|--------------|------------------------------------------|
| **cap-diameter**            | Quantitative | Float number in cm                       |
| **cap-shape**               | Qualitative  | bell=b, conical=c, convex=x, flat=f, sunken=s, spherical=p, others=o |
| **cap-surface**             | Qualitative  | fibrous=i, grooves=g, scaly=y, smooth=s, shiny=h, leathery=l, silky=k, sticky=t, wrinkled=w, fleshy=e |
| **cap-color**               | Qualitative  | brown=n, buff=b, gray=g, green=r, pink=p, purple=u, red=e, white=w, yellow=y, blue=l, orange=o, black=k |
| **does-bruise-bleed**       | Qualitative  | bruises-or-bleeding=t, no=f             |
| **gill-attachment**         | Qualitative  | adnate=a, adnexed=x, decurrent=d, free=e, sinuate=s, pores=p, unknown=? |
| **gill-spacing**            | Qualitative  | close=c, distant=d, none=f              |
| **gill-color**              | Qualitative  | see cap-color                            |
| **stem-height**             | Quantitative | Float number in cm                       |
| **stem-width**              | Quantitative | Float number in mm                       |
| **stem-root**               | Qualitative  | bulbous=b, swollen=s, club=c, cup=u, equal=e, rhizomorphs=z, rooted=r |
| **stem-surface**            | Qualitative  | see cap-surface                          |
| **stem-color**              | Qualitative  | see cap-color                            |
| **veil-type**               | Qualitative  | partial=p, universal=u                   |
| **veil-color**              | Qualitative  | see cap-color                            |
| **has-ring**                | Qualitative  | ring=t                                   |
| **ring-type**               | Qualitative  | cobwebby=c, evanescent=e, flaring=r, grooved=g, large=l, pendant=p, sheathing=s, zone=z, scaly=y, movable=m, none=f, unknown=? |
| **spore-print-color**       | Qualitative  | see cap color                            |
| **habitat**                 | Qualitative  | grasses=g, leaves=l, meadows=m, paths=p, heaths=h, urban=u, waste=w, woods=d |
| **season**                  | Qualitative  | spring=s, summer=u, autumn=a, winter=w  |

### Licensing

All source code and data are open-source and available for modification under the **Creative Commons License CC BY 4.0**.
