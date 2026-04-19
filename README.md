# Breast Cancer Wisconsin Classification

End-to-end ML project classifying breast tumors as malignant or benign 
from fine-needle aspirate (FNA) cell nucleus features.

## Dataset
- UCI Breast Cancer Wisconsin Diagnostic (569 patients, 30 features)
- 63% benign, 37% malignant
- Loaded via ucimlrepo package, no missing values

## Methods
- Train/test split (80/20) with stratification
- Feature scaling with StandardScaler
- Logistic Regression baseline
- Random Forest comparison

## Results

| Model | Accuracy | AUC | False Negatives |
|-------|----------|-----|-----------------|
| Logistic Regression | 96.5% | 0.996 | 3 |
| Random Forest | 97.4% | 0.993 | 3 |

## Top features (Random Forest)
Area, concave points, radius, and perimeter of the "worst" nuclei 
(mean of 3 largest) dominated the predictions — aligning with established 
cytological criteria for malignancy.

## Why this matters
Near-perfect classification performance on real pathology data using 
interpretable ML methods. The model independently converged on features 
that match clinical pathology reasoning.
