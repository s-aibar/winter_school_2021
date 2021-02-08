# cisTopic on 10X 5k PBMCs dataset

cisTopic (Bravo González-Blas *et al.*, 2019) is an R/Bioconductor package for the simulataneous identification of cis-regulatory topics and cell states from single cell epigenomics data. cisTopic relies on an algorithm called Latent Dirichlet Allocation (LDA), a robust Bayesian method used in text mining to group documents addressing similar topics and related words into topics. Interestingly, this model has a series of assumptions that are fulfilled in single-cell epigenomics data, such as non-ordered features (‘bag of words’) and the allowance of overlapping topics (i.e. a regulatory region can be co-accessible with different other regions depending on the context, namely, the cell type or state).

![alt text](https://github.com/dagousket/winter_school_2021/blob/master/tutorial/cistopic.png?raw=true)

In this tutorial, we will use a publicly available [10X dataset](https://support.10xgenomics.com/single-cell-atac/datasets/1.0.1/atac_v1_pbmc_5k) on peripheral blood mononuclear cells (PBMCs), consisting of scATAC-seq data from 5335 cells. This data has been pre-processed using cellRanger to provide a count matrix where rows correspond to cell barcodes and columns correspond to ATAC-seq peak genomic regions. The count inside this sparse matrix correspond to the number of non-duplicated fragment present in each cell within each genomic region. In addition cellRanger provide a metrics.csv file, summarising quality-check measures on a per-cell basis. Importantly, this file include information on which cell barcodes have been considered as real cell to creat the count matrix.

The analysis of this dataset will be decomposed into 5 parts :

1- running the LDA algorithm on the raw count data

2- analysing the cell-topic contribution matrix

3- analysing the region-topic contribution matrix

4- analysisng the region-cell predicitive matrix

5- export to loom file

![alt text](https://github.com/dagousket/winter_school_2021/blob/master/tutorial/cistopic_ws.001.png?raw=true)
