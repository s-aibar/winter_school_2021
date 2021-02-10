## Single cell transcriptomics, Gene regulatory networks and identification of cell states in space and time through single-cell transcriptomics and epigenomics (SCENIC, cisTopic)


![alt text](https://github.com/dagousket/winter_school_2021/blob/master/image_scenic_citopic.png?raw=true)

### Workshop overview

This workshop will be focused on inferring gene regulatory networks (GRNs) from single-cell RNA-seq and single-cell ATAC-seq data. The workshop will be split into two parts, one with each technology, both using the Peripheral blood mononuclear cells (PBMC) dataset from 10x genomics as a tutorial example.

To infer Gene Regulatory Networks from scRNA we will use [SCENIC](https://github.com/aertslab/SCENIC). SCENIC uses a random forest approach to link Transcription Factor (TFs) to their target genes based on gene expression co-variability across cells. By incorporation motif enrichment information, SCENIC further prunes the TF-target links (i.e. regulons) based on the presence of the TF binding motif in the cis-regulatory regions of the target genes. To identify cell states based on the activity of the network, it further calculates an activity score for each regulon based on the target genes expression level ranking in each cell.

SCENIC will  be run through [VSN](https://github.com/vib-singlecell-nf), a Nextflow processing pipeline which also includes quality-check process to filter good quality cells and is followed by standard dimensionality reduction analysis (t-SNE, UMAP, clustering, marker genes). The exploration of the obtained regulons and scores will be performed in R using a Jupyter environment, and the web-based visualization tool [SCope](https://scope.aertslab.org).

The scATAC analysis will be performed using the R package [cisTopic](https://github.com/aertslab/cisTopic). This package comprises a dimensionality reduction analysis based on Latent Dirichlet Allocation algorithm (LDA), which enables to probabilistically assign each cell and each genomic location to a "topic". Topics correspond to global or cell-type specific trends in the dataset, which will be used as latent variables for dimensionality reduction analysis (t-SNE, UMAP, clustering). In a second part, the tutorial will focus on the exploration of the obtained topics, notably the enrichment of ChIP-seq signatures and transcription binding motifs for individual topics.

The analysis will be performed in R using a Jupyter environment.

SCope session with anlaysis on complete datasets can be found here : https://scope.aertslab.org/#/qlife_winter_school/*/welcome

Html preview of the tutorials:
- [GRNs-SCENIC_Notebook_1_Running_VSN.html](https://rawcdn.githack.com/dagousket/winter_school_2021/69fb5aaa6a2cb6c0503caf76734bd0316b722f40/tutorial/GRNs_SCENIC/GRNs-SCENIC_Notebook_1_Running_VSN.html)
- [GRNs-SCENIC_Notebook_2_Exploring_output.html](https://rawcdn.githack.com/dagousket/winter_school_2021/69fb5aaa6a2cb6c0503caf76734bd0316b722f40/tutorial/GRNs_SCENIC/GRNs-SCENIC_Notebook_2_Exploring_output.html)
- [cistopic_tutorial_5kPBMC.html](https://rawcdn.githack.com/dagousket/winter_school_2021/83d5bc8d1885773128a425d0eeeda486bc61f954/tutorial/cisTopic/cistopic_tutorial_5kPBMC.html)
