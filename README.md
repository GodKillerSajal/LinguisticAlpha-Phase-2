# LinguisticAlpha Phase 2: Project Replication and Results

## Overview
This repository contains the code and dataset for LinguisticAlpha Phase 2, an empirical finance study investigating the relationship between executive linguistic patterns during earnings calls and subsequent cumulative abnormal returns (CAR).

## Primary Results
Our analysis yields three primary conclusions:

1. **Linguistic Risk Penalty**: A composite Linguistic Risk Score (LRS), which aggregates uncertainty, evasiveness, readability decline, and tone shifts, has a statistically significant negative coefficient (β = -0.015, t = -3.81) predicting [−5, +10] day CAR, even after controlling for standard Fama-French factors.
2. **Causal Identification via SCM**: Synthetic Control spatial placebo tests confirm that the price drop following high-risk linguistic calls is causally linked to the communication style itself, not merely underlying fundamental distress.
3. **Q&A Sentiment Superiority**: Transformer-based NLP (FinBERT) demonstrates that spontaneous linguistic leakage during the Q&A session carries significantly higher predictive validity regarding future returns than the heavily curated prepared remarks.

This notebook executes the entire analytical pipeline end-to-end without requiring manual intervention. The pipeline includes:
- Text preprocessing and LRS sub-index construction.
- Fama-French factor regressions (M1 to M5).
- Synthetic Control Method (SCM) estimations.
- Latent Dirichlet Allocation (LDA) topic modeling and orthogonalization.

*Note: The notebook is configured to use the `seaborn-v0_8-whitegrid` visual theme for optimal readability. Ensure all standard data science dependencies (`pandas`, `numpy`, `matplotlib`, `seaborn`, `statsmodels`, `scikit-learn`, `textstat`) are installed in your environment prior to execution.*
