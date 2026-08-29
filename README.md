# CO-CGN: High-Fidelity Cultural Heritage

Implementation and experimental resources for CO-CGN-based high-fidelity cultural heritage reconstruction, structural analysis, and evaluation.

## Overview

This repository contains the implementation structure, experimental scripts, evaluation utilities, and visualization resources associated with the CO-CGN framework for high-fidelity cultural heritage analysis.

The project focuses on comparing baseline approaches with the proposed CO-CGN framework and evaluating reconstruction and classification performance across different cultural heritage structural categories.

The structural categories considered in the experiments are:

- Architectural
- Sculptural
- Artifact
- Other

## Project Structure

```text
CO-CGN-High-Fidelity-Cultural-Heritage/
│
├── README.md
│
├── data/
│   └── README.md
│
├── preprocessing/
│   ├── gaussian_filter.py
│   ├── zscore.py
│   └── pca.py
│
├── models/
│   ├── cnn.py
│   ├── gnn.py
│   ├── coa.py
│   └── co_cgn.py
│
├── experiments/
│   ├── five_fold.py
│   ├── ablation_analysis.py
│   └── statistical_analysis.py
│
├── evaluation/
│   ├── classification_metrics.py
│   ├── structural_metrics.py
│   └── image_quality_metrics.py
│
├── visualization/
│   └── plots.py
│
├── results/
│   ├── tables/
│   └── figures/
│
├── requirements.txt
│
└── LICENSE
```

## Evaluation Metrics

### Classification Metrics

The classification experiments evaluate:

- Accuracy (%)
- Recall (%)
- F1-Score (%)
- AUC (%)

### Structural Reconstruction Metrics

The structural evaluation considers:

- Chamfer Distance ↓
- Hausdorff Distance ↓
- Point-to-Surface Error ↓
- Normal Consistency ↑
- F-Score (%) ↑

### Image Quality Metrics

Image-quality evaluation includes:

- PSNR (dB) ↑
- SSIM ↑

### Optimization Metrics

Optimization experiments can additionally report:

- Convergence Time (s)
- Fitness Evaluations

Lower values are preferable for distance, error, convergence-time, and FID-type measures, while higher values are preferable for accuracy, recall, F1-score, AUC, normal consistency, F-score, PSNR, and SSIM.

## Experimental Analysis

The repository is organized to support the following analyses.

### Five-Fold Evaluation

Five-fold cross-validation is used to obtain run-level performance estimates and average results.

### Ablation Analysis

The component analysis examines combinations involving:

- Gaussian filtering
- Z-score normalization
- PCA
- CNN
- GNN
- COA

The proposed CO-CGN configuration combines the components specified by the experimental design.

### Statistical Analysis

CO [Baseline] and CO-CGN [Proposed] can be compared using paired run-level results.

The statistical analysis reports:

- Mean
- Standard deviation
- 95% confidence interval
- p-value
- Significance

Significance notation:

```text
*    p < 0.05
**   p < 0.01
***  p < 0.001
NS   p >= 0.05
```

Statistical tests should be performed using independent run-level observations rather than a single averaged value.

## Dataset

The project uses a high-fidelity cultural heritage dataset for the experimental analysis.

Dataset files should be placed under:

```text
data/
```

If the dataset is subject to redistribution restrictions, the raw dataset should not be committed to the repository. Instead, provide the appropriate dataset source and acquisition instructions in `data/README.md`.

## Installation

Clone the repository:

Create a Python environment:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Reproducibility

For reproducible experiments:

- Use the same dataset version for all experiments.
- Keep the train/test or cross-validation partitioning consistent.
- Use fixed random seeds where applicable.
- Record the configuration and hyperparameters for every experiment.
- Preserve the five run-level results used for statistical analysis.
- Do not replace run-level measurements with averaged values before significance testing.

## Results

Experimental outputs can be organized under:

```text
results/
├── tables/
└── figures/
```

Recommended result files include:

```text
five_fold_results.csv
ablation_analysis.csv
structural_category_comparison.csv
co_vs_cocgn_statistical_test.csv
```

Figures can include:

- Classification performance comparisons
- Ablation/component analysis
- Structural-category comparisons
- Five-fold performance variation
- Statistical significance visualizations
- Reconstruction quality comparisons

## Reproducibility and Data Integrity

Reported experimental values should be generated from the corresponding implementation and evaluation data.

Structural metrics such as Chamfer Distance, Hausdorff Distance, Point-to-Surface Error, and Normal Consistency require suitable reference and reconstructed geometric data.

Similarly, PSNR and SSIM require corresponding reference and reconstructed image/rendering pairs.

These metrics should not be estimated or manually fabricated when the required evaluation data are unavailable.

## License

This repository is released under the license specified in `LICENSE`.

Before redistributing datasets, pretrained models, or third-party resources, verify that their respective licenses permit redistribution.

## Acknowledgement

This repository is intended to support transparent experimentation, reproducibility, and further research in high-fidelity cultural heritage analysis and reconstruction.
