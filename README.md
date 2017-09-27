# CDA-for-Clustering

This repository contains functions for using community detection analysis to cluster data.

cda_clustering_corr constructs the network based on the correlaitons between observations. Importantly this function expects that the data will be organzied such that the rows are individual observations and the columns are the features.

cda_clustering_dist constructs the network based on the euclidean distances between the observations. 

Both of the above mentioned functions use the edge betweenness community detection algorithim provided by the igraph package and therefore the igraph package must be installed in order for the functions to work.
Further the functions must be passed a data set in the form of a matrix or dataframe and the indeces of the columns to compute the correlations or distances. You can also set the 'sensitivity' argument (default of .001) to higher or lower values depending on how sensity you want the function to be when defining links in the network.
The functions return a single vector containing the cluster membership for each of the observations. 

For a companion article on using CDA for clustering see the following RPub: http://rpubs.com/JFLandrigan/CDA_Clustering. 
