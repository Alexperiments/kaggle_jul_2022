# kaggle_jul_2022
Tabular Playground Series - Jul 2022


## Best model so far: BGM for meta labels, MLP (400, 200, 100) for supervised classification
## Public Score: 0.81193

## Tasks
- [x] BGM clustering
- [x] Meta labels with a simple network (200, 100), score: 0.59855
- [x] Test higher thresholds for confidence prob. when choosing labels (testata 95%, score: 0.58857) (87% sembra meglio di 80%)
- [x] Feature engineering:
  - [x] found that categorical data are actually integers, which are apparently drawn from the same Poisson distribution (lam=50)
  - [x] found that only 14/30 features are meaningful
- [x] Try to use every feature in the MLP
- [x] Try deeper networks (didn't work)
- [x] Batch normalization (stabilizes the performance, not a great improvement)
- [x] Verify that the meta labels are balanced (they weren't but balancing them leads to a very small improvement ~0.0006)
- [x] Silhuette analysis per capire numero di clusters (best cluster is confirmed to be 7)
- [x] Check if data are repeated in the features
- [x] Auto-encoder for feature distillation (worsening in performance ~ 12%)
- [x] Reverse auto-encoder (decoder-encoder) to map the features in a higher-dimensional space
- [x] Starting from our best prediction (~0.61) train a BGMClassifier and then fit-predict the data
- [x] Combine the previous step with soft voting
- [x] Use the best prediction as labels iteratively (this improves the public score but probably it is probably overfitting)
