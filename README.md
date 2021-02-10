## Single cell transcriptomics, Gene regulatory networks and identification of cell states in space and time through single-cell transcriptomics and epigenomics (SCENIC, cisTopic)


### Workshop overview

This workshop will be focused on inferring gene regulatory networks (GRNs) from single-cell RNA-seq and single-cell ATAC-seq data. The workshop will be split into two parts, one with each technology, both using the Peripheral blood mononuclear cells (PBMC) dataset from 10x genomics as a tutorial example.

To infer Gene Regulatory Networks from scRNA we will use [SCENIC](https://github.com/aertslab/SCENIC). SCENIC uses a random forest approach to link Transcription Factor (TFs) to their target genes based on gene expression co-variability across cells. By incorporation motif enrichment information, SCENIC further prunes the TF-target links (i.e. regulons) based on the presence of the TF binding motif in the cis-regulatory regions of the target genes. To identify cell states based on the activity of the network, it further calculates an activity score for each regulon based on the target genes expression level ranking in each cell.

SCENIC will  be run through [VSN](https://github.com/vib-singlecell-nf), a Nextflow processing pipeline which also includes quality-check process to filter good quality cells and is followed by standard dimensionality reduction analysis (t-SNE, UMAP, clustering, marker genes). The exploration of the obtained regulons and scores will be performed in R using a Jupyter environment, and the web-based visualization tool [SCope](https://scope.aertslab.org).

The scATAC analysis will be performed using the R package [cisTopic](https://github.com/aertslab/cisTopic). This package comprises a dimensionality reduction analysis based on Latent Dirichlet Allocation algorithm (LDA), which enables to probabilistically assign each cell and each genomic location to a "topic". Topics correspond to global or cell-type specific trends in the dataset, which will be used as latent variables for dimensionality reduction analysis (t-SNE, UMAP, clustering). In a second part, the tutorial will focus on the exploration of the obtained topics, notably the enrichment of ChIP-seq signatures and transcription binding motifs for individual topics.

The analysis will be performed in R using a Jupyter environment.
