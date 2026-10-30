# Worked Solutions — Clustering and Unsupervised Learning

The following answers are starting points. Scores may differ if you change the data, split, or parameters.

## 1. Identify the business question, target variable, and unit of observation.

**Target and grain:** for churn, each row is one synthetic customer and `churn` is a binary label. For sales, each row is a synthetic weekly store observation with `weekly_sales` as the target. For segmentation, no target is provided.

## 2. Load the relevant CSV and report row and column counts.

`pd.read_csv("data/customer_churn_synthetic.csv").shape` (from repository root).

## 3. Check the dataset for null values and duplicate rows.

`df.isna().sum()` and `df.duplicated().sum()`; interpret whether repeated IDs represent duplicate records or separate events.

## 4. Compute a descriptive summary of numeric features.

`df.describe().T`; compare mean, median, and range.

## 5. Explain why a train/test split is required.

A holdout estimates generalization to unseen observations; random splits are unsuitable for temporal leakage scenarios.

## 6. Create an 80/20 split with random_state=42.

`train_test_split(X, y, test_size=0.2, random_state=42, stratify=y)` for classification; omit `stratify` for regression.

## 7. Choose a sensible naive baseline and explain its limits.

For classification use `DummyClassifier(strategy="most_frequent")`; for regression use `DummyRegressor(strategy="mean")`.

## 8. Fit the model in Examples.ipynb and report its score.

Execute `Examples.ipynb` and record the printed metrics and data split.

## 9. Explain one plausible form of data leakage.

Fitting a scaler or imputer before the split exposes test-set information to training; put it inside a pipeline.

## 10. Change one model parameter and compare outcomes using cross-validation.

Use `cross_val_score` on training data and compare average scores, then evaluate the selected model on held-out test data once.

## 11. Create a plot and write two observations without causal claims.

Plot a histogram with `df.select_dtypes("number").iloc[:,0].hist()`; describe distribution, skew, and any outliers without implying causality.

## 12. Write a five-sentence model card: purpose, data, evaluation, limitations, next step.

**Example model card:** Purpose: predict synthetic churn. Data: 800 generated customer rows. Evaluation: stratified holdout and cross-validation. Limitations: synthetic features and unknown real-world shift. Next step: validate on authorized representative production data.
