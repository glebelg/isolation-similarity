# Isolation Similarity


<p align="right"><b>
"Two points in a sparse region are more similar than two points of equal inter-point distance in a dense region"
</b></p>

<p align="right"><b>
[arXiv:1907.00378v1]
</b></p>


In this work I implemented Isolation Kernel (Similarity) using iForest and aNNE. Isolation Kernel is described in the article "Nearest-Neighbour-Induced Isolation Similarity and Its Impact on Density-Based Clustering" [arXiv:1907.00378v1](https://arxiv.org/pdf/1907.00378.pdf). I used datasets "jain" and "pathbased" from [cs.uef.fi](http://cs.uef.fi/sipu/datasets) and "Breast Cancer Wisconsin (Diagnostic)" from [archive.ics.uci.edu](https://archive.ics.uci.edu/ml/datasets).
Algorithm MBSCAN based on iForest- and aNNE-Dissimilarity are compared with DBSCAN, SpectralClustering, AgglomerativeClustering.

| dataset \ algorithm | agglomerative_clustering |	dbscan | mbscan_aNNE | mbscan_iForest | spectral_clustering |
| --- | --- | --- | --- | --- | --- |
| jain | 0.769 | 0.828	| 1.000 | 1.000 | 0.87 |
| pathbased | 0.732 | 0.699 | 0.988 | 0.747 | 0.732000 |
| wdbc | 0.856 | 0.577 | 0.930 | 0.906 | 0.830 

As we see, the best algorithm on all datasets is algorithm based on Isolation Kernel – MBSCAN-aNNE. The second algorithm in terms of quality is another one based on Isolation Kernel – MBSCAN-iForest.|
