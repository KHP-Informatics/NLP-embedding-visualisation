# NLP-embedding-visualisation
This repo contains supplementary interactive visualisations for the paper

The visualisations are available here: [https://khp-informatics.github.io/NLP-embedding-visualisation/](https://khp-informatics.github.io/NLP-embedding-visualisation/)

# Available visualisations
## Patient embedding
[LINK](https://khp-informatics.github.io/NLP-embedding-visualisation/embedding.html)

![Screenshot of the embedding](/imgs/embedding.png)

Clustering of patients based on SNOMED disorder codes detected in free text. A sample of 100,000 patients was embedded based on normalised annotation counts for all SNOMED disorder codes detected in at least 1000 patients at King's College Hospital. These vectors were reduced to 50 dimensions using PCA then to 2 dimensions using t-SNE. Colour indicates cluster membership (50 clusters) assigned by agglomerative clustering with Ward linkage.


The prevalence of SNOMED codes is calculated for each cluster and the count of each code is propagated up the SNOMED ontology to all parents. The following SNOMED codes are then removed as they are uninformative (most have 100% prevalence in all clusters as they are high level parent codes): 138875005, 64572001, 301857004, 123946008, 118234003, 404684003, 362965005. When a cluster is selected, up to 5 codes are shown. These are the most prevalent codes that are relevant to at least 50% of the patients in the cluster.

For performance reasons, this visualisation is further subsampled to 20% of the original data, stratified by cluster.

## Treemap - top 100 concepts and "others" (v1)
[LINK](https://khp-informatics.github.io/NLP-embedding-visualisation/treemap.html)

![Screenshot of the treemap with other group](/imgs/treemap_v1.png)

Hover over a concept to see the concept name and total annotation (the number of times the concept was detected, not the number of patients). Click a type (finding, disorder, substance) to expand those annotations. Click "all" to return to the overview. Only the top 100 concepts per type are shown, all remaining concepts per type are merged into the "other" group, and the number in brackets indicates the number of merged concepts.

## Treemap - top 100 concepts only (v2)
[LINK](https://khp-informatics.github.io/NLP-embedding-visualisation/treemap_no-other.html)

![Screenshot of the treemap without other group](/imgs/treemap_v2.png)

Hover over a concept to see the concept name and total annotation (the number of times the concept was detected, not the number of patients). Click a type (finding, disorder, substance) to expand those annotations. Click "all" to return to the overview. Only the top 100 concepts per type are shown.

# Authors
Daniel Bean, Zeljko Kraljevic, Anthony Shek, James Teo, Richard Dobson

# Cite
TBC

# Acknowledgements
This work uses data provided by patients and collected by the NHS as part of their care and support. We would like to thank the patients on the Kings Electronic Records Research Interface (KERRI), the NIHR Applied Research Centre South London, the NIHR Maudsley Biomedical Research Centre, the London AI Centre for Value-based Healthcare, the NHS AI Lab and Health Data Research (UK).

# Funding
The project has received funding support from Innovate UK, NHS AI Lab, Office of Life Sciences, Health Data Research UK, NIHR Maudsley Biomedical Research Centre and NIHR Applied Research Centre South London.