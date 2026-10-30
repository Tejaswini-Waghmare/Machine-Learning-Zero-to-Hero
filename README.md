# Machine Learning Zero to Hero

A structured, beginner-friendly collection of **10 machine-learning modules** with runnable Python notebooks, 120 practice tasks, worked guidance, and three fully synthetic datasets.

> **Learning materials, not production deployments.** Synthetic datasets do not establish real-world model performance.

## Modules
- [Machine Learning Foundations](01_ML_Fundamentals/README.md) — Problem framing, features, targets, supervised vs unsupervised learning, train/test split, baseline models.
- [Data Preparation and Pipelines](02_Data_Preprocessing/README.md) — Missing values, scaling, encoding, pipelines, leakage prevention, column transformers.
- [Regression Models](03_Regression/README.md) — Linear regression, ridge, regularization, MAE, RMSE, R-squared, residual analysis.
- [Classification Models](04_Classification/README.md) — Logistic regression, decision trees, random forests, confusion matrices, precision and recall.
- [Evaluation and Cross-Validation](05_Model_Evaluation/README.md) — Holdout testing, cross-validation, ROC-AUC, precision-recall, imbalanced classes, threshold selection.
- [Ensemble Learning](06_Ensemble_Learning/README.md) — Bagging, random forests, gradient boosting, bias-variance tradeoff, feature importance limitations.
- [Clustering and Unsupervised Learning](07_Unsupervised_Learning/README.md) — K-means, standardization, silhouette score, PCA, cluster interpretation.
- [Feature Engineering and Selection](08_Feature_Engineering/README.md) — Feature interactions, polynomial features, feature selection, validation-safe transforms.
- [Hyperparameter Optimization](09_Hyperparameter_Tuning/README.md) — GridSearchCV, parameter grids, nested validation concepts, model selection, test-set integrity.
- [End-to-End Machine Learning Projects](10_End_to_End_ML_Projects/README.md) — Churn risk ranking, model comparison, business interpretation, reproducibility, limitations.

## Quick start

```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

Open a notebook from the repository root, then **Run All**. Each notebook loads data from `data/` or `../data/` automatically. In Colab, upload all three CSV files into the Colab file pane first.

## Data dictionary

- `customer_churn_synthetic.csv`: customer_id, six numerical features, binary churn target. Feature values are generated abstract variables and are **not real dollar amounts or months**, despite human-readable labels.
- `store_sales_synthetic.csv`: five abstract numerical predictors and a synthetic continuous weekly_sales target (not actual USD).
- `customer_segments_synthetic.csv`: three synthetic numeric dimensions for clustering.

## Reproducibility and limitations
Datasets generated with scikit-learn random_state=42; model examples set random_state where supported. Random train/test splits are appropriate for these IID synthetic examples, not automatically for chronological or grouped real-world data. Do not represent generated results as company outcomes.

## Suggested portfolio improvements
Run all notebooks, add output screenshots, compare models, write model cards, and document assumptions.
