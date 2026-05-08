# CSCI 3329 — Homework 3 Report
## 1. Dataset
- Name: Statlog (Vehicle Silhouettes)
- source: https://archive.ics.uci.edu/dataset/149/statlog+vehicle+silhouettes
- number of samples: 946
- number of classes: 4	OPEL, SAAB, BUS, VAN
- number of features: 18
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
- I used Forward/Backward Selection search method because my number of features are 18. With this many features the Exhaustive Search would have taken the already long run time(4 hrs) to a ridiculous amount.
- For the  RepeatedKFold protocol I used n_repeats=3 because the runtime went above 3 hours

| Algorithm           | Best Feature Subset                                                                                                                                                                               | Mean Accuracy | Std     |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|---------|
| Linear Classifier   | 'COMPACTNESS', 'DISTANCE_CIRCULARITY', 'SCATTER_RATIO', 'ELONGATEDNESS', 'MAX_LENGTH_RECTANGULARITY', 'SCALED_RADIUS_GYRATION', 'SKEWNESS_MAJOR', 'KURTOSIS_MAJOR', 'HOLLOWS_RATIO'               | 0.6703        | 0.0641  |
| Logistic Regression | 'COMPACTNESS', 'CIRCULARITY', 'DISTANCE_CIRCULARITY', 'MAX_LENGTH_ASPECT_RATIO', 'MAX_LENGTH_RECTANGULARITY', 'SCALED_VARIANCE_MAJOR', 'SKEWNESS_MAJOR', 'SKEWNESS_MINOR', 'KURTOSIS_MAJOR'       | 0.7340        | 0.0437  |
| KNN                 | 'COMPACTNESS', 'CIRCULARITY', 'PR_AXIS_ASPECT_RATIO', 'MAX_LENGTH_ASPECT_RATIO', 'SCATTER_RATIO', 'ELONGATEDNESS', 'MAX_LENGTH_RECTANGULARITY', 'SCALED_VARIANCE_MINOR', 'SCALED_RADIUS_GYRATION' | 0.7412        | 0.0471  |
| Gaussian NB         | 'COMPACTNESS', 'PR_AXIS_ASPECT_RATIO', 'ELONGATEDNESS', 'MAX_LENGTH_RECTANGULARITY', 'SCALED_VARIANCE_MAJOR', 'SKEWNESS_MAJOR', 'SKEWNESS_MINOR', 'KURTOSIS_MAJOR', 'HOLLOWS_RATIO'               | 0.5587        | 0.0507  |
| Neural Network      | 'COMPACTNESS', 'RADIUS_RATIO', 'PR_AXIS_ASPECT_RATIO', 'MAX_LENGTH_ASPECT_RATIO', 'PR_AXIS_RECTANGULARITY', 'MAX_LENGTH_RECTANGULARITY', 'SKEWNESS_MAJOR', 'KURTOSIS_MAJOR', 'HOLLOWS_RATIO'      | 0.8291        | 0.0383  |

## 5. Discussion
- Part 2 vs Part 3 comparison
- Per-algorithm observations:
- Linear Classifier:
- Logistic Regression:
- KNN:
- Gaussian NB:
- Neural Network: This algorithm takes around 10 times longer than the other algorithms, but it is the most accurate algorithm

- Limitations and ideas for improvement
## 6. Reproduction
- python 3.14
- libraries: pandas, numpy, and sklearn
- Run command (e.g., `python main.py`)
