# End-to-End Machine Learning Projects

**Module:** `10_End_to_End_ML_Projects`  
**Level:** beginner to intermediate  
**Data:** synthetic; no real customer or business records.

## Learning objectives
- Churn risk ranking
- Model comparison
- Business interpretation
- Reproducibility
- Limitations

## Key ideas
A practical project includes a question, data dictionary, leakage-safe split, baseline, tuned model, metrics, business action, limitations, and reproducible run instructions.

### Practical interpretation
The supplied notebook demonstrates this topic using deliberately synthetic data. Its numerical results are illustrative; they are not evidence of a production model.

### Formulas and metrics
- Mean: $\bar{x}=\frac{1}{n}\sum_i x_i$
- MAE: $\frac{1}{n}\sum_i |y_i-\hat y_i|$
- Precision: $TP/(TP+FP)$; Recall: $TP/(TP+FN)$
- Always evaluate with a metric matched to the business cost.


## Reproducible workflow
1. Define a question and target before selecting an algorithm.
2. Inspect data shape, schema, missingness, and label distribution.
3. Split data before fitting transforms or tuning.
4. Fit preprocessing on training folds only; use a pipeline.
5. Compare against a simple baseline and report relevant metrics.
6. Use held-out data once for final evaluation; document uncertainty and limitations.

## Common pitfalls
- Leakage from using the test set to choose features, thresholds, or hyperparameters.
- Treating accuracy as sufficient for imbalanced classification.
- Treating correlation or feature importance as causation.
- Publishing synthetic examples as real business outcomes.
- Reporting metrics without the evaluation split, random seed, or class balance.

## Reflection prompts
- What does a false positive cost in this scenario?
- Would a simpler model be easier to deploy and explain?
- How might distribution shift change the results?
