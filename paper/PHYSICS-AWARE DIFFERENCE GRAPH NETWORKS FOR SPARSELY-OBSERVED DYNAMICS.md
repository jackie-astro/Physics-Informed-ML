PHYSICS-AWARE DIFFERENCE GRAPH NETWORKS FOR SPARSELY-OBSERVED DYNAMICS

Author: Sungyong Seo Chuizheng Meng Yan Liu

## Challenges:
The discretization error becomes even larger when the sparse data are irregularly distributed or defined on an unstructured
grid, making it hard to build deep learning models to handle physics-governing observations on the unstructured grid.
 
* Core Concepts: Modeling Physics Phenomena with Limited Observations

<img width="350" alt="knowledge-aware" src="https://github.com/jqwenchen/PIML/blob/master/paper/imgs/4.png">

## Summary:
This paper proposes a novel architecture, Physics-aware Difference Graph Networks (PA-DGN), which exploits neighboring 
information to learn finite differences inspired by physics equations. PA-DGN leverages data-driven end-to-end learning to 
discover underlying dynamical relations between the spatial and temporal differences in given sequential observations.

<img width="750" alt="knowledge-aware" src="https://github.com/jqwenchen/PIML/blob/master/paper/imgs/3.png">

Inspired by the property, the paper first proposes spatial difference layer (SDL) to efficiently learn the local representations by 
aggregating neighboring information in the sparse data points. The layer is based on graph networks (GN) as it easily leverages 
structural features to learn the localized representations and share the parameters for computing the localized features
 
Then, the layer is followed by recurrent graph networks (RGN) to predict the temporal difference which is another core 
component of physics-related dynamic equations. PA-DGN is applicable to various tasks and two representative tasks are provided;
the approximation of directional derivatives and the prediction of graph signals.
