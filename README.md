# Using-Seurat-for-scRNASeq-Analyses-in-GenePattern

Using Seurat for scRNASeq Analyses in GenePattern 

## Input Data 

For this tutorial, we will be analyzing a dataset of Peripheral Blood Mononuclear Cells (PBMCs), freely available from 10X Genomics. 
There are 2,700 single cells that were sequenced on the Illumina NextSeq 500 and ran through the Cell Ranger pipeline. the original files can be found here. 

Note that this is a compressed folder which contains three files:  

matrix.mtx: Triples of gene ID index, cell barcode index, and UMI count. 
* barcodes.tsv: The barcodes referenced by the indices in the matrix.mtx file. 
* features.tsv: All the annotated genes, one per row. Referenced by the indices in the matrix.mtx file. 
* This file is sometimes named genes.tsv 

The steps below encompass the standard pre-processing workflow of scRNA-seq data in Seurat. We have split it in 3 sequential steps corresponding to:  
* Data loading and visualization of QC metrics. 
* Data filtering, normalization, scaling, and dimensionality reduction. 
* Clustering.
