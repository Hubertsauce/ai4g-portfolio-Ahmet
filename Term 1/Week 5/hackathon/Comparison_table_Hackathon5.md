# Comparison table

All models were tuned with 5-fold stratified cross-validation on the training set (26,029 rows), using **balanced accuracy** as the main metric. The test set (6,508 rows) was used only once, at the end. Precision, recall and F1 are calculated for the positive class: **low income (`<=50K`)**.

| Model | Best hyperparameters | CV balanced accuracy (mean ± std) | Test balanced accuracy | Test precision | Test recall | Test F1 |
|---|---|---|---|---|---|---|
| **Dummy (baseline)** | `strategy="most_frequent"` | 0.500 ± 0.000 | 0.500 | 0.759 | 1.000 | 0.863 |
| Simple rule | `education.num <= 10` | not cross-validated (0.669 on the training set) | 0.667 | 0.849 | 0.761 | 0.802 |
| KNN | `n_neighbors=21` | 0.766 ± 0.009 | 0.773 | 0.884 | 0.928 | 0.906 |
| Logistic regression | `C=1`, `class_weight="balanced"` | 0.821 ± 0.006 | 0.820 | 0.940 | 0.803 | 0.866 |
| **Gradient boosting** (recommended) | `learning_rate=0.1`, `max_depth=4` (fixed: `max_iter=200`, `class_weight="balanced"`) | **0.843 ± 0.008** | **0.845** | **0.951** | 0.824 | 0.883 |

## How to read this table

- **Balanced accuracy** is our main metric, because the data is imbalanced (76% low income). The dummy scores 0.500 on it, which is the same as guessing.
- **The dummy's recall of 1.000 and F1 of 0.863 look good, but are misleading.** The dummy labels everyone as low income, so it misses no one, but it also contacts all 1,568 people with a higher income.
- **KNN has the highest recall** (it misses only 354 low-income people), but it wrongly contacts 600 people with a higher income.
- **Gradient boosting has the best balanced accuracy and precision.** It misses 870 low-income people, but wrongly contacts only 209 people with a higher income.
- **The test scores are close to the CV scores**, so the cross-validation results were reliable.
