# review-starembed

Notes on reproducing **StarEmbed: Benchmarking Time Series Foundation Models on Astronomical Observations of Variable Stars**.

| | |
| --- | --- |
| Paper | [arXiv:2510.06200](https://arxiv.org/abs/2510.06200) |
| Venue | [ICML 2026 Workshop on AI for Physics](https://ai4physics-workshop.github.io/) |
| Code | [skai-institute/StarEmbed](https://github.com/skai-institute/StarEmbed/tree/41f6220d9e37203543745cd6c110f1f9ad5635cc) @ `41f6220` |

## 2 November 2026

**Proposal.** Check whether the released pipeline reproduces the clustering result for frozen Chronos-tiny embeddings on ZTF variable stars: Table 2, row Chronos, ARI (K-Means) `0.1596 (0.0029)`. The follow-up is to rerun the experiment across random seeds and see how K-Means initialization changes the score.

**Smoke test.** A 70-object subset of ZTF (10 stars per class) was embedded with Chronos-T5-tiny and Chronos-Bolt-tiny, then clustered with the paper's K-Means and Ward setup. Recorded metrics are ARI, NMI, and macro-F1, together with a t-SNE plot and a dendrogram.

Notebook: [starembed_validation.ipynb](starembed_validation.ipynb)
