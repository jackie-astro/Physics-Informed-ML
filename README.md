# Knowledge-Aware-ML
This repo will contain multiple topics including Neural Differential Equations, Physics Informed ML, Casual Learning, and my understandings to those topics, etc. 

## Physics-aware ML Paper and Notes

- When Physics Meets Machine Learning: A survey of Physics-Informed Machine Learning [paper](https://arxiv.org/pdf/2203.16797.pdf) 
  <details><summary>Notes</summary>
	A well-round survey including ML for Physics, Physics for ML, etc.
  </details>
  
  
- Neural Ordinary Differential Equations  [paper](https://arxiv.org/pdf/1806.07366.pdf) [note](https://github.com/jqwenchen/KIML/blob/master/paper/ODE-note.pdf)
  <details><summary>Notes</summary>
	How ODE’s can be used to solve data modelling problems-> solving problems using the muscle power of neural networks.
  </details>

- Physics-aware Difference Graph Networks For Sparsely-Observed Dynamics  [paper](https://openreview.net/pdf?id=r1gelyrtwH) [code](https://github.com/jqwenchen/PIML/tree/master/PADGN) 
  <details><summary>Notes</summary>
        ** Previous code has some bugs, and cannot work with PyG2.0, re-Implement, now compatible wth PyG2.0 **
	
	Physics on continuous Domain + Sparse and irregular observed points = Time Series at obaserved points
  </details>
  
- Coupled Multiwavelet Operator Learning for Coupled Differential Equations  [paper](https://openreview.net/pdf?id=kIo_C6QmMOM) 
  <details><summary>Notes</summary>
        Partial differential equations (PDEs) are key tasks in modeling the complex dynamics of many physical processes.
  </details>
  
  
## Casual-aware ML Paper and Notes
 ### Basic Knowledge with Casual Learning and Casual Discovery
   #### Casual Inference Three Stairs
  
  1. The first level is association, since it refers to a purely statistical association, determined entirely by our observational data.
  2. The second level is Intervention, which is more complex than correlation because it involves not just what we see, but changing what we see.
  3. The third level is counterfactuals, (Structural Casual Model) Counterfactuals are placed at the top of the hierarchy because they include intervening and relational questions. If a model is devised that can answer counterfactuals, it can also answer questions about interventions and observations.
  

   #### Difference between Intervention and Counterfactuals
 
   This difference can be distinguished by the actual application scenario. If the question we want to answer is that there is no scene in the data that requires us to observe, then it can be considered as a counterfactual; In short, the data after the second layer of intervention may contain other observed variables to assist in the completion.
   
   #### Classes of Causal Structural Learning / Causal Discovery  
   	
	A:  Constraint-based approaches : build causal graphs by conditional independence tests (PC; Fast Causal Inference; PCMCI)
	B: Score based learning algorithms based on penalized Neural Ordinary Differential Equations
	C: Convergent Cross Mapping (CCM): tackles the problems of nonseparable weakly connected dynamic systems by reconstructing nonlinear state space
	D: Approaches based on Additive Noise Model
	E: Granger causality approach: analyze the temporal causal relationships by testing the aid of a time-series on predicting another time-series. 
		
 ### Paper and Notes with Casual Learning and Casual Discovery
 
- Towards Causal Representation Learning  [paper](https://arxiv.org/pdf/2102.11107.pdf) 
  <details><summary>Notes</summary>
        
	1. describe different levels of modeling in physical systems and present the differences between causal and
        statistical models (including Predicting in the i.i.d. setting, Predicting Under Distribution Shifts, Answering Counterfactual Questions,
	                    and Nature of Data: Observational, Interventional,(Un)structured)
	
	2. review existing approaches to learn causal relations from appropriate descriptors
	
	3. discuss how useful models of reality may be learned from data in the form of causal representations, and discuss several current problems of
	   machine learning from a causal point of view
	
	4. assay the implications of causality for practical machine learning
	
  </details>

- Causal Inference in Recommender Systems: A Survey and Future Directions  [paper](https://arxiv.org/pdf/2208.12397.pdf) 
  <details><summary>Notes</summary>
        Causal Inference in Recommender Systems
  </details>


- A Survey on Causal Reinforcement Learning  [paper](https://arxiv.org/pdf/2302.05209.pdf) 
  <details><summary>Notes</summary>
        Causal Reinforcement Learning
  </details>

- Estimating Treatment Effects from Irregular Time Series Observations with Hidden Confounders  [paper](https://idevede.github.io/pdf/LipCDE.pdf) [note](https://github.com/jqwenchen/PIML/blob/master/paper/Estimating%20Treatment%20Effects%20from%20Irregular%20Time%20Series%20Observations%20with%20Hidden%20Confounders.md)
  <details><summary>Notes</summary>
        Causal analysis for time series data: estimating individualized treatment effect
  </details>
  
  
- CUTS: NEURAL CAUSAL DISCOVERY FROM IRREGULAR TIME-SERIES DATA  [paper](https://openreview.net/pdf?id=UG8bQcD3Emv) 
  <details><summary>Notes</summary>
        To address the issue of model's  degeneration performance when encountering data with randomly missing entries or non-uniform sampling frequencies,
	CUTS is proposed as a neural Granger causal discovery algorithm to jointly impute unobserved data points and build causal graphs, via plugging in           two mutually boosting modules in an iterative framework:
		 
   1. Latent data prediction stage: designs a Delayed Supervision Graph Neural Network (DSGNN) to hallucinate and register irregular data                      which might be of high dimension and with complex distribution; 
	
   2. Causal graph fitting stage: builds a causal adjacency matrix with imputed data under sparse penalty.
	
  </details>
  

  
