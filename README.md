# Pull Request Acceptance Prediction Using Machine Learning

## Background

This project builds on an existing research dataset that analyzes GitHub Pull Requests using structured metadata such as:

- pull request structure  
- repository popularity signals  
- contributor and AI agent usage  
- programming language  
- commit-level change statistics  

The dataset contains metadata and change summaries, but does **not include full source code snapshots**. The original research focused mainly on descriptive analysis of AI-assisted pull requests rather than prediction.

---

## Project Extension

This project extends the dataset into a **predictive modeling task** - predicting whether a Pull Request will be accepted using machine learning.

The notebook demonstrates:

- model building and comparison  
- multiple hyperparameter variants  
- metric interpretation beyond ROC-AUC  
- threshold tuning behavior  
- robustness and stability testing  
- baseline encoding sensitivity checks  
- subgroup (bias) performance checks  
- feature importance interpretation  

---

## Models Evaluated

Two model families were tested with multiple configurations:

- Logistic Regression  
- Random Forest  

Evaluation metrics include:

- ROC AUC  
- PR AUC  
- Precision / Recall  
- F1 Score  
- Accuracy  

---

## Key Findings

- Logistic Regression and Random Forest achieved similar performance (~0.60 ROC AUC range)
- Hyperparameter changes affected coefficient magnitude but not feature ranking
- Decision threshold strongly affects the precision–recall tradeoff
- Feature importance rankings remain stable across alternate baseline encodings
- Subgroup performance variation is mostly driven by sample size differences

---

## Scope Limitation

This project uses structured PR metadata only.  
Code quality and semantic code analysis are out of scope because full code content is not available in the dataset.
