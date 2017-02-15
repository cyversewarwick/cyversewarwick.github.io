---
layout: post
title: "Application Access Guide"
date: 2017-02-14
---

There are 3 options when it comes to using our applications:

1. Via the CyVerse Discovery Environment. This is the recommended approach to a new user. This is the easiest option since a full user interface is provided to the user.
2. Using the Docker images that are available on our [Docker Hub repository](https://hub.docker.com/u/cyversewarwick/). Each application/tool has a corresponding image.
3. With the source codes that are hosted on our [Github repository](https://github.com/cyversewarwick)

We give details on the first option and interested users may try the other two options with reference to the documentations we have for each application.

## CyVerse Discovery Environment

All of our applications on the [CyVerse Discovery Environment](https://de.cyverse.org/) are searchable using the "**uk cyverse**" keyword in the application search box.

Below is a screenshot showing the search in action:
![Search for CyVerse UK apps](https://cyversewarwick.github.io/images/Search_Apps.png)

A full list of applications developed by the Warwick team is given in the table:

| Application | Description | Run on CyVerse \* |
| --- | :---: | --- |
|  | *Sequence Alignment* |  |
| [APPLES](https://github.com/cyversewarwick/apples) | A set of tools to analyse promoter sequences on a genome-wide scale| [DE](https://de.cyverse.org/de/?type=apps&app-id=d99ca952-dbe2-11e6-9e37-0242ac120003) |
|  | *Footprint Identification* |  |
| [Wellington Bootstrap](https://github.com/cyversewarwick/wellington-bootstrap) | An algorithm for the identification of regions occupied by proteins in DNase-seq data, performing a differential analysis between two samples | [DE](https://de.cyverse.org/de/?type=apps&app-id=cbf83e84-1cf1-11e6-b710-0242ac120003) |
| [Wellington Footprint](https://github.com/cyversewarwick/wellington-footprint) | An algorithm for the identification of regions occupied by proteins in DNase-seq data | [DE](https://de.cyverse.org/de/?type=apps&app-id=035655fc-2736-11e6-ac3b-0242ac120003) |
|  | *Differencial Expression* |  |
| [GP2S](https://github.com/cyversewarwick/gp2s) | A differential expression algorithm for time series data with a two condition (eg. control/treated) experimental design | [DE](https://de.cyverse.org/de/?type=apps&app-id=655a8432-7432-11e6-a6f8-0242ac120003) |
| [Gradient Tool](https://github.com/cyversewarwick/gradienttool) | An algorithm for the identification of the time of change from single condition time course expression data | [DE](https://de.cyverse.org/de/?type=apps&app-id=11d9f454-78d4-11e6-9314-0242ac120003) |
|  | *Network Inference* |  |
| [CSI](https://github.com/cyversewarwick/csi) | A network inference algorithm capable of inferring causal regulatory network models from time course expression data | [DE](https://de.cyverse.org/de/?type=apps&app-id=12659e20-1c39-11e6-8842-0242ac120003) |
| [hCSI](https://github.com/cyversewarwick/hcsi) | An expansion of CSI network inference to handle multiple time course datasets | [DE](https://de.cyverse.org/de/?type=apps&app-id=ae88f3b0-1c3e-11e6-b0d6-0242ac120003) |
| [oCSI](https://github.com/cyversewarwick/ocsi) | An expansion of CSI network inference to handle data from multiple organisms | [DE](https://de.cyverse.org/de/?type=apps&app-id=429173d2-1c46-11e6-aaba-0242ac120003) |
|  | *Clustering / Biclustering* |  |
| [BHC](https://github.com/cyversewarwick/bhc) | A clustering algorithm for expression data originally made available in R, allows for the analysis of both time course or multiple static datasets | [DE](https://de.cyverse.org/de/?type=apps&app-id=1e03e32e-4e87-11e6-bd1d-0242ac120003) |
| [TCAP](https://github.com/cyversewarwick/tcap) | A clustering algorithm for time course expression data, identifies complex regulatory groups thanks to a rich information measure | [DE](https://de.cyverse.org/de/?type=apps&app-id=d874c350-ad90-11e6-a854-0242ac120003) |
| [Wigwams](https://github.com/cyversewarwick/wigwams) | An algorithm for the extraction of gene groups co-regulated across subsets of multiple time course datasets | [DE](https://de.cyverse.org/de/?type=apps&app-id=d5d04224-1cf8-11e6-81c4-0242ac120003) |
|  | *Transcription Factor Motif Enrichment* |  |
| [HMT](https://github.com/cyversewarwick/hmt) | A transcription factor binding site overrepresentation analysis algorithm for known motifs | [DE](https://de.cyverse.org/de/?type=apps&app-id=818d8ce0-5e4c-11e6-ac0d-0242ac120003) |
| [MEME-LaB](https://github.com/cyversewarwick/meme_lab) | A transcription factor binding site overrepresentation analysis algorithm with novel motif discovery | [DE](https://de.cyverse.org/de/?type=apps&app-id=b781fc48-8edd-11e6-b4ab-0242ac120003) |



\* - A CyVerse account is required. Register [here](https://user.cyverse.org/) if necessary.

These applications are also accessible through our [local Discovery Environment](https://cyverse.warwick.ac.uk/de)
