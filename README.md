# Target Kernel Design for Alignment-Based Multiple Kernel One-Class Classification

Code for the master's dissertation of the same title (CPGEI, Universidade Tecnológica Federal do Paraná, 2026).

A one-class SVM is trained on a weighted sum of RBF kernels. The weights come from kernel–target alignment with a *target kernel* built only from normal data (a kNN graph, a k-Means partition, or a spectral clustering).

| Path | Contents |
|---|---|
| `target-kernel-ocsvm.ipynb` | Produces every table and figure in the dissertation |
| `results/` | Stored per-fold results: main benchmark, sensitivity analysis, two ablations |
| `figures/` | Figures written by the notebook |

## Running it

```bash
pip install -r requirements.txt
jupyter lab target-kernel-ocsvm.ipynb
```

By default the notebook reads the stored results and runs in about a minute. Set `RUN_BENCHMARKS = True` and `RUN_SENSITIVITY = True` in Section 1 to refit everything (1–2 hours and several GB of RAM). Breast Cancer and Wine come with scikit-learn; the other datasets are downloaded from OpenML on first use.
