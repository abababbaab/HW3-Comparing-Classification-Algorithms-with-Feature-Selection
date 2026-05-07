# CSCI 3329 — Homework 3 Report
## 1. Dataset
- Name: Statlog (Vehicle Silhouettes)
- source: https://archive.ics.uci.edu/dataset/149/statlog+vehicle+silhouettes
- number of samples: 946
- number of classes: 4	OPEL, SAAB, BUS, VAN
- Class distribution (table or bar chart)
## 2. Preprocessing
- Data has no missing values 
- Encoded only y because data is already in numbers
- scaled data because some values are up to 200 and some are low to around 1
## 3. Part 2 — Algorithm Comparison
| Algorithm           | Mean Accuracy | Std     |
|---------------------|---------------|---------|
| Linear Classifier   | 0.7293        | 0.0553  |
| Logistic Regression | 0.7906        | 0.0433  |
| KNN                 | 0.7127        | 0.0461  |
| Gaussian NB         | 0.4575        | 0.0533  |
| Neural Network      | 0.8447        | 0.0370  |
## 4. Part 3 — Feature Selection
- Search method and justification
| Algorithm | Best Feature Subset | Mean Accuracy | Std |
|-----------|--------------------|---------------|-----|
## 5. Discussion
- Part 2 vs Part 3 comparison
- Per-algorithm observations
- Limitations and ideas for improvement
## 6. Reproduction
- Python version, key library versions
- Run command (e.g., `python main.py`)
