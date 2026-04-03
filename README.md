# Robustness Visualization Repository

This repository provides qualitative visualizations for robustness analysis of the nudity suppression mechanism under embedding perturbations.

The repository is released to facilitate transparency and reproducibility of the experiments described in the submission.

---

## 1. Robustness Evaluation

Two perturbation settings are evaluated:

- Case A: Random Semantic Replacement
- Case B: Gaussian Noise Perturbation

---

### Case A: Random Semantic Replacement

In this setting, a proportion $\rho$ of anchors are replaced with randomly sampled embeddings from the MS COCO dataset.

This simulates severe semantic corruption by introducing embeddings that are unrelated to the sensitive direction.

The replacement is performed at the embedding level, and the sampled COCO captions are non-sensitive and independent of the suppression task.

#### Example COCO Prompts Used for Replacement

The following examples illustrate the type of captions randomly sampled from MS COCO:

- A photo of a person.
- A photo of a car on the road.
- A photo of a dog in the grass.
- A photo of a cat sitting on a sofa.
- A photo of a bicycle next to a tree.
- A photo of a bus on a city street.
- A photo of a bird flying in the sky.
- A photo of a chair in a room.
- A photo of a dining table with food.
- A photo of a boat on the water.

These embeddings are used solely to simulate semantic replacement and evaluate robustness under extreme semantic shift.

#### Visualization

![Random Semantic Replacement](caseA.png)

---

### Case B: Gaussian Noise Perturbation

In this setting, Gaussian noise with varying standard deviation is added to the normal anchor embedding.

This simulates stochastic perturbations in the embedding space.

No semantic replacement is performed in this case.

The sensitive direction is recomputed after perturbation, and the generation seed is fixed for consistent comparison.

#### Visualization

![Gaussian Noise Perturbation](caseB.png)

---

## 2. Experimental Setting (Brief Description)

- Case A: A proportion $\rho$ of anchors are replaced with random MS COCO embeddings.
- Case B: Gaussian noise is added only to the normal anchor embedding.
- The suppression mechanism remains unchanged across settings.
- The generation seed is fixed for comparability.
- All results are qualitative.

---

No personal or institutional information is included to maintain anonymity during the review process.
