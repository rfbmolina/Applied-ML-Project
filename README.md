# B-Cell Epitope Prediction — Applied Machine Learning Project

This repository contains my final project for the **Applied Machine Learning for Engineering** module. The aim is to build and evaluate supervised learning pipelines for **linear B-cell epitope prediction** under **severe class imbalance**, engaging directly with modelling choices and the trade-offs that determine **generalisation**.

## Project summary
- **Task:** binary classification (epitope vs non-epitope)
- **Primary focus:** generalisation-aware evaluation and model selection under class imbalance
- **Models compared:** Random Forest vs fully connected feed-forward neural network (MLP)
- **Model selection metrics:** **F1** and **PR-AUC** (with ROC/PR analysis and threshold tuning)
- **Validation design:** **group-aware splitting / cross-validation** to reduce leakage across related samples

## Repository contents
- `Applied_ML_Project.ipynb` — end-to-end analysis, experiments, and results

## Method outline
1. **Data preparation**
   - Basic cleaning and preprocessing
   - Class imbalance inspection and baseline metrics
2. **Validation strategy (leakage control)**
   - Group-aware split / CV to prevent overly optimistic estimates from correlated samples
3. **Feature analysis**
   - Feature importance / reduction experiments where appropriate
4. **Modeling**
   - Random Forest baseline and tuned variants
   - MLP pipeline with hyperparameter sweeps
5. **Imbalance handling**
   - Resampling experiments (e.g., SMOTE / undersampling) where applicable
6. **Selection and evaluation**
   - Model selection driven by **F1** / **PR-AUC**
   - Threshold optimisation and ROC/PR curve reporting

## Key modelling decisions (what I learned)
This project prioritises *decision-making under constraints* rather than a single “best model”: I compare pipelines in terms of bias–variance behaviour, sensitivity to class imbalance, metric choice (accuracy vs PR-AUC/F1), and how validation design affects apparent performance and robustness.

## How to run
1. Clone the repository.
2. Open `Applied_ML_Project.ipynb` in Jupyter/VS Code.
3. Run cells top-to-bottom to reproduce preprocessing, training, and evaluation.

## Tech stack
- Python
- NumPy, pandas
- scikit-learn
- imbalanced-learn
- matplotlib

## Notes
This repository is for educational/research purposes (module coursework). It is not intended for clinical use.
