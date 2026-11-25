# DSC212 - Karate Club Modularity

**Name:** Ankit Thakur  
**Roll:** IMS25244
**Course:** DSC212: MATHEMATICAL FOUNDATION FOR DATA SCIENCE

## Overview
Implemented **Recursive Spectral Modularity Partitioning** from scratch on Zachary's Karate Club Graph. Instead of simply minimizing edge cuts, the algorithm uses the modularity matrix \(B = A - \frac{kk^T}{2m}\) to find communities that are statistically surprising compared to a random null model. The graph is recursively split using the leading eigenvector until no further modularity gain is possible.

## Repository Contents
- `DSC212_Karate_Modularity.ipynb`: Main notebook (runs top-to-bottom).
- `*GRAPHS.ZIP`: Visualizations of graph splits, node metric evolution, and Modularity \(Q\) vs. Ground Truth (ARI/NMI) PRODUCED OUTPUT IMAGES.

## Key Findings
- The first split almost perfectly recovers the historical two-faction split.
- Nodes **0 (Mr. Hi)** and **33 (Officer)** consistently remain the top hubs and bridges.
- Further recursive splits increase the Modularity Score but overfit the graph, reducing agreement with the actual historical outcome.

## Setup
```bash
pip install numpy networkx matplotlib scikit-learn pandas
