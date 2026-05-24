# Chronic-Kidney-Disease-Classification

Chronic kidney disease (CKD) is a progressive condition characterised by the gradual loss of renal function over time (NHS, 2023). Approximately 7.2 million people are affected by CKD in the UK, and in 2023 it was ranked the ninth leading cause of death globally (Mark et al., 2025). Despite its burden, CKD remains frequently undetected in early stages due to its asymptomatic nature. Patients often present only after significant or irreversible renal damage has occurred.

This project develops and evaluates machine learning models for binary CKD classification using the National Health and Nutrition Examination Survey (NHANES) dataset. It also explores SHAP analysis and subgroup analysis.

### Objectives
- Clean and prepare dataset.
- Perform exploratory data analysis.
- Apply feature transformation and encoding.
- Train and compare classification models.
- Evaluate models' performance using clinically relevant metrics. 
- Perform explainability and subgroup analysis.

### Prerequisites
- Python 3.13
- Jupyter notebook

### Installation step 
- Install the required packages: 
  ```pip install -r requirements.txt```

The dataset is a curated cohort derived from NHANES. It was obtained from kaggle and specifically prepared for CKD machine learning tasks. It contains 11,933 observations and 29 variables including demographic, lifestyle, laboratory, and clinical features. 

- The dataset can be downloaded from: https://www.kaggle.com/datasets/alitaqishah/ckd-nhanes-2021-2023-staged-kidney-disease
- The dataset should be placed in the directory and renamed as 'CKD_NHANES_2021_2023.csv'

### How to run
Open the jupyter notebook and run all cells from top to bottom.

 
### Tools and libraries used
- Python 3.13
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- SHAP
- Matplotlib and seaborn
- ydata-profiling


### Steps
#### Data overview and cleaning
- Data profiling
- Handling missing values
- Handling outliers

#### Exploratory data analysis
- Understanding data distributions
- Summary statistics

#### Transformation
- Log transformation
- Categorical encoding
  
#### Model development
- Modelling with clinical biomarkers
- Modelling without clinical biomarkers
  Models:
  - Logistic regression
  - Random forest
  - XGBoost

#### Model evaluation
- Comparison of model performance
- Hyperparameter tuning
- Threshold adjustment
- Metrics used:
    - Recall
    - Precision
    - ROC-AUC
    - F1-Score
    - Accuracy (less emphasis)

#### Model explainability
- SHAP analysis

#### Model uncertainity and calibration
- Evaluating model calibration to assess reliablity of probabilities predicted
#### Subgroup analysis
- Evaluating model sensitivity across demographic groups
#### Results
After adjusting the threshold, logistic regression outperformed XGBoost and random forest with a recall of 0.806. Recall was prioritised as the primary metric because the cost of false negatives is very high in chronic kidney disease diagnosis. SHAP analysis identified age as the strongest predictor, followed by uric acid and ethnicity.
















