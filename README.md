# More Robots, Better Manners? Federated Continual Learning and A Multi-robot, Multi-view Dataset

## Overview
This is a PyTorch-based code implementation accompanying the Advanced Robotics Research submission [More Robots, Better Manners? Federated Continual Learning and A Multi-robot, Multi-view Dataset](https://arxiv.org/abs/2405.15773). 
### Abstract
It is critical for robots to explore Federated Learning (FL) settings where several robots, deployed in parallel, can learn independently while also sharing their learning with each other. This collaborative learning in real-world environments requires social robots to adapt their actions to dynamically changing, unpredictable situations and varying task settings. Under these conditions, the social appropriateness of robot actions depends on several factors, including the robot’s embodiment and environmental conditions. However, the scarcity of datasets captured from multi-view, multi-robot perspectives makes this problem difficult to address with existing machine learning and continual learning frameworks. In this work, we explore a simulated living room environment in which different robots must learn the social appropriateness of their actions. First, we present the MannersDB+ dataset, which contains thousands of scenes for three different robots (Pepper, NAO, and PR2) from multiple viewpoints, along with human-annotated social appropriateness labels for a range of robot actions (e.g., vacuuming, carrying objects, starting a conversation). Using this dataset, we introduce Federated Root (FedRoot) averaging, a novel weight aggregation strategy which disentangles feature learning across clients from individual task-based learning. Finally, to adapt to challenging environments, we extend FedRoot to Federated Latent Generative Replay (FedLGR), a novel Federated Continual Learning (FCL) strategy that uses FedRoot-based weight aggregation and embeds each client with a generator model for pseudorehearsal of learnt feature embeddings to mitigate forgetting in a resource-efficient manner. Our results show that FedRoot-based methods offer competitive performance while also resulting in a sizeable reduction in resource consumption (up to 86% for CPU usage and up to 72% for GPU usage). Additionally, our results demonstrate that FedRoot-based FCL methods outperform other methods while also offering an efficient solution (up to 84% CPU and 92% GPU usage reduction), with FedLGR providing consistently strong performance across evaluations. 

## Table of Contents

- [MannersDB+ Dataset](#dataset)
- [Installation](#installation)
- [Training](#training)
- [Citation](#citation)
- [Acknowledgement](#acknowledgement)

## MannersDB+ Dataset
The dataset folder contains example scenes from Pepper, NAO and PR2 robots, and the full dataset will be publicly available after acceptance.

## Installation

Ensure you have the necessary dependencies installed. Run the following command to set up the environment:

```bash
pip install -r requirements.txt
```


## Training

### Federated Learning
FL strategies are implemented as python packages. To execute the code on MANNERS-DB run the following:

```bash
bash run_FL_local.sh
```
Make sure all necessary paths are provided correctly. 

### Federated Continual Learning
FCL strategies are alsoimplemented as python packages. To execute the code on MANNERS-DB run the following:

```bash
bash run_CL_local.sh
```
Make sure all necessary paths are provided correctly. 


## Citation

```
@misc{Churamani2024Feature,  
  author        = {N. {Churamani} and F.I. {Dogan} and S. {Checker} and Y. {Malladi} and H.T.L {Chiang} and H. {Gunes}},  
  title         = {{Feature Aggregation with Latent Generative Replay for Federated Continual Learning of Socially Appropriate Robot Behaviours}},   
  year          = {2025},  
  eprint        = {},
  archivePrefix = {arXiv},
  primaryClass  = {cs.LG}
 }
```

## Acknowledgement
**Funding:** [N. Churamani](https://nchuramani.github.io), [F.I. Dogan](https://www.irmakdogan.com), [Y. Malladi] (), and [H. Gunes](https://www.cl.cam.ac.uk/~hg410/) are with the Department of Computer Science and Technology, University of Cambridge, UK.
[S. Checker](https://www.sakshamchecker.com) is with King's College London, UK, and contributed to this work while undertaking a remote visiting studentship at the Department of Computer Science and Technology, University of Cambridge. 
[H.T.L. Chiang](https://sites.google.com/view/lewispro/home) is with Google DeepMind.
This work is supported by Google under the GIG funding scheme. The authors also thank Jie Tan and Carolina Parada for their valuable feedback.

**Open Access:** For open access purposes, the authors have applied a Creative Commons Attribution (CC BY) licence to any Author Accepted Manuscript version arising.

**Data Access Statement:** The dataset will be publicly only upon accaptance.

