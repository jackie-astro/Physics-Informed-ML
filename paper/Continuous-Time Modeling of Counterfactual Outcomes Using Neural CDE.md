Author: Nabeel Seedat  Fergus Imrie Alexis Bellot Zhaozhi Qian Mihaela van der Schaar


## Basic Knowledge

1. ATE ：Average Treatment Effect
2. ATT ：Average Treatment Effects on Treated
3. CATE：Conditional Average Treatment Effect
4. ITE：Individual Treatment Effect


## Challenges:

1. Existing causal inference approaches typically consider regular, discrete-time intervals between observations and treatment decisions and
hence are unable to naturally model irregularly sampled data, which is the common setting in practice. 

2. Estimating counterfactual outcomes in the longitudinal setting introduces additional challenges, the most significant of which is that 
the observed treatment assignment may depend on confounding variables that vary over time. (e.g: not all cancer patients are equally likely 
to be offered the same chemotherapy regimen.) Specifically, history of patients’ covariates and their response to past treatments affects 
future treatments. This can introduce bias in causal effects and variance in the estimation of counterfactuals due to the systematic 
differences in the distribution of confounding variables between any two sets of treatments over time.

## Summary:

TE-CDE(Treatment Effect Neural Controlled Differential Equation)
To handle arbitrary observation patterns, we interpret the data as samples from an underlying continuous-time process and propose to 
model its latent trajectory explicitly using the mathematics of controlled differential equations.

"Neural ODE and its extensions have been considered for modeling irregular time series data. However, NeuralODE-type methods are 
conventional time series models, which do not account for issues such as time-dependent confounding."

<img width="750" alt="knowledge-aware" src="https://github.com/jqwenchen/PIML/blob/master/paper/imgs/5.png">


In addition, adversarial training is used to adjust for time-dependent confounding which is critical in longitudinal settings and is an
added challenge not encountered in conventional time-series.


* Key components to facilitate the modeling of counterfactual outcomes in continuous time are as follows:

1.   TE-CDE’s encoder learns a representation that is defined continuously in time (i.e. a continuous latent path), rather
than only at discrete time steps.
2.   The latent path trajectory evolves as a response of a Neural Controlled Differential Equation (CDE).
3.   Decoding and prediction are in continuous-time.
4.   TE-CDE uses domain adversarial training to learn a representation that adjusts for time-dependent confounding
and hence is suitable for causal estimation.





