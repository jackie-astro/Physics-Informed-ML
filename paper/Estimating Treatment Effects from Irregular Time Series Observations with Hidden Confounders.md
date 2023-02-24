Estimating Treatment Effects from Irregular Time Series Observations with Hidden Confounders

Author: Defu Cao James Enouen Yujing Wang Xiangchen Song Chuizheng Meng Hao Niu Yan Liu


## Challenges:

1. the existence of hidden confounders can lead to biased treatment estimates and complicate the causal inference process
2. in continuous time settings with irregular samples, it is challenging to directly handle the dynamics of causality
 
## Summary

LipCDE is proposed to solve the above challenges.
LipCDE can directly model the dynamic causal relationships between historical data and outcomes with irregular samples by considering the boundary of hidden confounders given by Lipschitz constrained neural networks
 
* Related Tasks
1) Treatment effects learning in the static setting
 
2) Treatment effects learning in the dynamic setting without hidden confounders
 
3) Treatment effect learning in the dynamic setting with hidden confounders

## Process

<img width="750" alt="knowledge-aware" src="https://github.com/jqwenchen/PIML/blob/master/paper/imgs/1.png">


LipCDE first infers the interrelationship of hidden confounders on treatment by bounding the boundary of hidden confounders via the hidden confounders boundary branch.
After that, LipCDE feeds the history trajectories into the synthetic control branch, which utilizes both observed data and hidden confounders to generate the latent representation of each patient.
Besides, we re-weight the population of all participating patients and balance the representation via applying a time-varying inverse probability of treatment weighting (IPTW) strategy. Combined with the LSTM layer, the outcome model can get the final estimate of the treatment effect.
