This notebook reconstructs single-cell RNA sequencing (scRNA-seq) data using a Masked AutoEncoder implemented in PyTorch, and performs hierarchical (Agglomerative) clustering on the learned latent embeddings.

The source code of scMAE is available at: https://zenodo.org/records/10465991

Libraries such as scanpy (for single-cell preprocessing) and scikit-learn (for clustering and evaluation) are used throughout the workflow.
Although alternative clustering methods (KMeans, Spectral, Leiden, DBSCAN) are implemented, the main analysis pipeline is based on AgglomerativeClustering with n_clusters = n_classes.

Workflow Overview

Data preparation and random gene masking

Training the Masked AutoEncoder for data imputation/reconstruction

Extracting latent embeddings from the encoder

Performing AgglomerativeClustering on the latent space

Evaluating performance with metrics such as NMI, ARI, Accuracy, and Silhouette Score, and saving the results as .csv

This workflow provides a unified framework for feature learning and hierarchical clustering in single-cell transcriptomics.

_____________________________________________________________________________________________________________________________________________
