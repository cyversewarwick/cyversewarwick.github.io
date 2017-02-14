---
title: Expression Data Analysis Pipeline
---

## Expression Data Analysis Pipeline

![Expression Data Analysis Pipeline](http://cyverseuk.org/wp-content/uploads/2016/07/Expression_Data_Analysis_Pipeline.png)

Performing an analysis of large-scale expression data can be a daunting task, as any relevant information on the effects of the monitored treatment are diluted by tens of thousands of profiles that are left unaffected by the condition change. The Warwick team of CyVerse UK set out to create a number of apps that can get you from normalised expression time course data to concise biological hypotheses on regulatory functionality. It should be noted that these tools were created with array data in mind, but you are welcome to use count data as well. If this is the case, remember to log-transform your data before feeding it into the apps.

The first step of an analysis is typically the identification of differentially expressed genes (DEGs), often coupled with temporal deconstruction to help sequence the order of relevant events. This goes a long way towards reducing the size of the data and helping you focus on the genes that carry the signal you are trying to decipher. [GP2S](http://cyverseuk.org/applications/gaussian-process-two-sample-gp2s-test-of-differential-expression/) is an algorithm that allows for the detection of differential expression between two conditions of a time course, and also features an extension that allows for the detection of the time when the gene becomes differentially expressed. If your time course data only features one condition, then the gradient tool is a more fitting method of identifying the timing of events as it is created with a single condition time course dataset in mind. The method can also be potentially used for DEG identification by deeming the genes that get picked up by the method as changing at some point in time to be differentially expressed.

Once in possession of a differentially expressed gene list, further size reduction can be done by performing clustering and biclustering. Algorithms belonging to those families aim to split the data up into groups exhibiting related behaviour. [BHC](http://cyverseuk.org/applications/bayesian-hierarchical-clustering-bhc/) is a hierarchical clustering algorithm that requires minimal user input, and can be used successfully on both time course and static data. [TCAP](http://cyverseuk.org/applications/temporal-clustering-by-affinity-propagation-tcap/) allows a different clustering experience, as the method uses a more complex similarity measure and produces intricate clusters that can feature regulatory interactions extending beyond mere co-regulation. If you're in possession of multiple time course datasets (such as different conditions), you can try [Wigwams](http://cyverseuk.org/applications/wigwams/), which will mine them for modules of genes co-regulated across at least two of the provided datasets.

Gene groups obtained from the above methods can then be mined for relevant biological information, putting the detected expression trends into context. Two common forms of enrichment analysis are GO terms and transcription factor binding sites. In terms of GO term analysis, all the clustering/biclustering methods support the [Cytoscape](http://www.cytoscape.org/) plugin [BiNGO](http://apps.cytoscape.org/apps/bingo), with one of the output files serving as direct input for BiNGO's overrepresentation analysis. Two CyVerse apps allow for the analysis of transcription factor binding sites - MEME-LaB performs *de novo* mining, detecting novel overrepresented motifs, while [HMT](http://cyverseuk.org/applications/hypergeometric-motif-test-hmt/) screens promoters for known transcription factor binding sites. Once again, input files compatible with the apps are provided on output from the clustering/biclustering apps.


Another potential analysis is the identification of underlying regulatory networks. Such models, inferred based on transcription factor expression levels, show the signalling chains of transcription factors, helping put the observed downstream co-regulatory events captured by clusters/biclusters into context. [CSI](http://cyverseuk.org/applications/causal-structure-inference-csi/) proposes a model based on how good a job upstream transcription factors' expression profiles do of explaining the downstream transcription factors' expression profiles at a later time point, and the resulting model can be turned into a [Cytoscape](http://www.cytoscape.org/)-friendly network by applying a stringency threshold on the confidence in each edge. Extensions of the algorithm exist - [hCSI](http://cyverseuk.org/applications/hierarchical-causal-structure-inference-hcsi/) can infer related networks across multiple datasets, while [oCSI](http://cyverseuk.org/applications/orthologous-causal-structure-identification-ocsi/) can worth with data captured from different species.