# Regulatory Text Classification with Uncertainty Estimation

This project implements a regulatory text classification system for ECOA, FCRA, and TILA, augmented with uncertainty estimation to support risk-aware decision-making.

## Overview

Standard classifiers produce predictions regardless of confidence. This system extends a traditional pipeline by incorporating uncertainty signals that enable abstention when predictions are unreliable.

Pipeline:
- Word2Vec embeddings for semantic representation
- Logistic Regression for classification
- Entropy (uncertainty) and margin (confidence) scoring
- Abstention mechanism for high-uncertainty cases

## Key Features

- Semantic text embeddings (Word2Vec)
- Probabilistic classification (Logistic Regression)
- Entropy-based uncertainty estimation
- Margin-based confidence measurement
- Abstention strategy for risk mitigation
- Multi-run reproducibility analysis
- Artifact generation for traceability

## Artifacts

### Figures
- `entropy_distribution.png`
- `margin_distribution.png`
- `confusion_matrix.png`

### Results
- `results_run_baseline.csv`
- `results_run1.csv`
- `results_run2.csv`
- `results_run3.csv`
- `run_summary.csv`

### Notebook
- `Regulatory_Text_Classification_Uncertainty.ipynb`

## Reproducibility

The pipeline was executed multiple times to assess stability. Due to stochastic initialization in Word2Vec:

- Predictions remain largely consistent
- Uncertainty (entropy) shows minor variation

All run outputs are saved to support reproducibility and artifact-based evaluation.

## How to Run

1. Open the notebook in Google Colab  
2. Run all cells from top to bottom  

Outputs include:
- predictions
- uncertainty metrics
- saved figures
- multi-run artifacts

## Interpretation

- Entropy → prediction uncertainty  
- Margin → separation between top classes  
- Abstention → defers uncertain predictions  

This enables a more reliable, risk-aware classification system.

## Limitations

- Small synthetic dataset  
- Static embeddings (no contextual modeling)  
- Limited regulatory coverage  

## Future Work

- Contextual models (e.g., BERT)
- Retrieval-augmented classification
- Larger datasets
- Improved uncertainty calibration

## Artifact Availability

All artifacts, including figures, run outputs, and the full notebook, are available in this repository.

## Note

This project emphasizes uncertainty-aware modeling, reproducibility, and responsible AI design.
