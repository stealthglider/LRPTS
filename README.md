# STEP: Learning STructured Embeddings for Progressive Time Series

This repository contains code and resources for learning latent representations in progressive time series data.

## Contents

- **`/figures`**: Contains figures from HI evaluations.
- **`/CMAPSS`**: Includes code for training models on various datasets, a Jupyter notebook for interactive analysis, and scripts for running additional experiments.
- **`/vinograd`**: Contains Vinograd’s mouse neural activity data and related scripts.

## Setup

### Data Preparation

To unzip the CMAPSS dataset, run the following command in your terminal:

```bash
unzip data.zip
```

This will extract the dataset into the current directory.

## Figures

![Approach Overview](/figures/0.fig1.png)   

Figure 1. Approach overview. a) Model Learning using triplet sampling. b) Latent Space Views c) Latent Space Indicators: We derive quantifiable indicators as an interface to the latent; namely the angular progression (θt) between prototype vectors or radius (r) from the z-space origin to disentangle the progression modes. These can be used as features/indicators for downstream tasks including prognostics, forecasting, and regime identification.

### latent, theta and r capture state, not t/T

![FD002 Example of latent HIs](/figures/FD002_latent_hi_distribution_comparison_tT.png) 

### FD004 CMAPSS t-SNE of latent trajectory from engine 20

![FD004 Example of latent HIs](/figures/FD004.png) 

It reflects the learned progressive representation of the underlying estimated health states. Proxy indicators such as the angular position and the radius permit to interface with the manifold, which can be useful for industrials in quest of health indicators. A downstream model takes this latent and derived indicators, and models temporal relationships while also mitigating noise present in the dataset towards downstream tasks, such as RUL prediction in CMAPSS. 
