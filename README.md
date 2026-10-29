# CO-CGN: High-Fidelity Cultural Heritage

Implementation and experimental resources for cultural heritage preprocessing, feature extraction, classification, reconstruction, and quality evaluation.

## Overview

This project focuses on high-fidelity cultural heritage analysis across four structural categories:

- Architectural
- Sculptural
- Artifact
- Other

The workflow includes image preprocessing, PCA-based feature extraction, classification, reconstruction assessment, and comparative performance evaluation.

## Methods

### Preprocessing
- Gaussian Filtering
- Z-Score Normalization

### Feature Extraction
- Principal Component Analysis (PCA)

### Classification and Reconstruction
- CO-CGN (Proposed Framework)
- Convolutional Neural Network (CNN)
- Graph Neural Network (GNN)
- Crayfish Optimization Algorithm (COA)

## Evaluation Metrics

**Classification Metrics**
- Accuracy (%)
- Recall (%)
- F1-Score (%)
- AUC (%)

**Structural Reconstruction Metrics**
- Chamfer Distance
- Hausdorff Distance
- Point-to-Surface Error
- Normal Consistency
- F-Score (%)

**Image Quality Metrics**
- Peak Signal-to-Noise Ratio (PSNR)
- Structural Similarity Index Measure (SSIM)

**Optimization Metrics**
- Convergence Time (s)
- Fitness Evaluations

## Experimental Analysis

The project supports five-fold evaluation, component-based ablation analysis, structural-category comparisons, and statistical testing using run-level results.

## Dataset

The dataset contains cultural heritage images and csv file for training and testing. Place the required data files in the appropriate project directories.

## Installation

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

## Results

Store experimental tables, evaluation metrics, and visualization outputs in the `results/` directory.

## Reproducibility

Use consistent data partitions, fixed random seeds where applicable, and actual evaluation outputs. Structural metrics require reference and reconstructed geometry, while PSNR and SSIM require corresponding reference and reconstructed images.

## License

Refer to the `LICENSE` file for usage and redistribution terms.
