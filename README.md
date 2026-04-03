# Robustness Visualization Repository

This repository provides qualitative visualizations and prompt lists used for robustness analysis under embedding perturbations.

The purpose of this repository is to facilitate transparency and reproducibility of the robustness experiments described in the submission.

---

## 1. Robustness Visualization

Two PNG files are included:

---

### (1) Random Irrelevant Embedding Injection

This visualization demonstrates the effect of injecting randomly sampled unrelated embeddings into the normal anchor.

It illustrates how the generation behavior changes when semantically irrelevant perturbations are introduced into the embedding space.

#### Visualization

![Random Irrelevant Embedding Injection](caseA.png)

---

### (2) Gaussian Noise Perturbation

This visualization demonstrates generation behavior under varying Gaussian noise strengths applied to the normal anchor embedding.

Different noise levels are applied to analyze robustness and stability of the sensitive direction under stochastic perturbations.

#### Visualization

![Gaussian Noise Perturbation](caseB.png)

These figures include representative failure cases and qualitative degradation patterns observed under perturbation.

---

## 2. Random COCO-style Prompts Used for Robustness Evaluation

The following randomly selected generic COCO-style prompts are used to evaluate robustness under embedding perturbations:

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

These prompts represent general, non-sensitive content and are used to examine generation stability under:

- Gaussian noise perturbation
- Random irrelevant embedding injection

All experiments are conducted under fixed random seeds to ensure comparability across perturbation settings.

---

## 3. Experimental Setting (Brief Description)

- Perturbation is applied only to the normal anchor embedding.
- The sensitive direction is recomputed after perturbation.
- The generation seed is fixed for consistent comparison.
- Visualization results are qualitative.

---

## 4. Notes

This repository is provided for qualitative inspection of robustness behavior under embedding perturbations.

No personal or institutional information is included to maintain anonymity during the review process.
