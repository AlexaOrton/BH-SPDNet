# BH-SPDNet
We generate synthetic block-hierarchical (BH) financial market correlation matrices. The SPDNet with Riemannian batch normalisation is used to learn on both this synthetic data and correlation matrices of the JSE Top 60 stock price returns.

The nested price return process is an adaptation/parameterised version of the general model proposed by Hierarchically Nested Factor Model from Multivariate Data (Tumminello et al., 2007) https://doi.org/10.1209/0295-5075/78/30006 and expanded on in Agglomerative Likelihood Clustering (Yelibi and Gebbie, 2021) https://doi.org/10.1088/1742-5468/ac3661 with code repo: https://github.com/lyelibi/timeseries_generator

The basic architecture of the SPDNet with Riemannian batch normalisation is informed by the work of Brooks et al. (2019) in Second-Order Networks in pytorch https://doi.org/10.1007/978-3-030-26980-7_78; http://arxiv.org/abs/1909.02414. Olivier Schwander's formulation of the NN-optimisation-functional form of the iterative problem-solving approach is found at https://gitlab.lip6.fr/schwander/torchspdnet. 
