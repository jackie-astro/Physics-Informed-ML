# Knowledge-Awared-ML
This repo will contain multiple topics including Casual Learning, Physics Informed ML, and my understandings to those topics, etc. 

## Physics-aware ML Paper and Code

- Neural Ordinary Differential Equations  [paper](https://arxiv.org/pdf/1806.07366.pdf) [code](https://github.com/jqwenchen/PIML/tree/master/NeuralODE)
  <details><summary>Notes</summary>
	How ODE’s can be used to solve data modelling problems-> solving problems using the muscle power of neural networks.
  </details>

- Physics-aware Difference Graph Networks For Sparsely-Observed Dynamics  [paper](https://openreview.net/pdf?id=r1gelyrtwH) [code](https://github.com/jqwenchen/PIML/tree/master/PADGN)
  <details><summary>Notes</summary>
        ** Previous code has some bugs, and cannot work with PyG2.0, re-Implement, now compatible wth PyG2.0 **
	
	Physics on continuous Domain + Sparse and irregular observed points = Time Series at obaserved points
  </details>
  
## Casual-aware ML Paper and Notes
 ### Basic Knowledge with Casual Learning and Casual Discovery
   #### Casual Inference Three Stairs
  
  1. The first level is association, since it refers to a purely statistical association, determined entirely by our observational data.
  2. The second level is Intervention, which is more complex than correlation because it involves not just what we see, but changing what we see.
  3. The third level is counterfactuals, (Structural Casual Model) Counterfactuals are placed at the top of the hierarchy because they include intervening and relational questions. If a model is devised that can answer counterfactuals, it can also answer questions about interventions and observations.
  
   <img width="450" alt="knowledge-aware" src="https://github.com/jqwenchen/PIML/blob/master/paper/imgs/2.png">

   #### Difference between Intervention and Counterfactuals
 
   This difference can be distinguished by the actual application scenario. If the question we want to answer is that there is no scene in the data that requires us to observe, then it can be considered as a counterfactual; In short, the data after the second layer of intervention may contain other observed variables to assist in the completion.

 ### Paper and Notes with Casual Learning and Casual Discovery

- Estimating Treatment Effects from Irregular Time Series Observations with Hidden Confounders  [paper](https://idevede.github.io/pdf/LipCDE.pdf) [note](https://github.com/jqwenchen/PIML/blob/master/paper/Estimating%20Treatment%20Effects%20from%20Irregular%20Time%20Series%20Observations%20with%20Hidden%20Confounders.md)
  <details><summary>Notes</summary>
        Causal analysis for time series data: estimating individualized treatment effect
  </details>
  
  
  
  
