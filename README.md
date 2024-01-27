# Applied-ML-on-Rheumatology
This project was done with collaboration with MAD Lab institute FAU university. 
The dataset is protected and is not sharable.

## Abstract
This repository presents a study on the use of machine learning (ML) techniques to predict the effectiveness of methotrexate (MTX) treatment on rheumatoid arthritis (RA) patients. The objective is to create a predictive algorithm using clinical, serologic, genomic, and sociodemographic data from early RA patients to predict the effectiveness of drug treatment in 24 weeks before continuing with other synthetic or biologic antirheumatic drugs. The study focuses on using iterative imputation instead of simple imputation of missing values and optimizing model performance and computation speed through hyperparameter tuning using the optuna method. Several popular supervised machine learning models are applied, including Random Forest, Adaboost, XGBoost, SVM, and LightGBM, to determine the best-performing model for predicting patient responses to MTX treatment.

## Introduction
Rheumatoid Arthritis (RA) is characterized by joint pain, and research has been conducted to optimize treatment costs, drug consumption, and identify effective clinical properties for remission rate improvement. Machine Learning (ML) has been increasingly applied in medical applications, including personalized therapy, drug discovery, and medical imaging analysis. ML enables personalized treatment plans based on individual patient characteristics, offering tailored treatment recommendations to optimize outcomes and minimize side effects.

## Materials and Methods
### Data Acquisition and Participants
Follow-up data of 387 patients treated with methotrexate was gathered from Erlangen-University Hospital.

### Clinical Outcomes and Definition of Response
Sociodemographic, clinical, and genomic data at baseline were used to predict response to methotrexate treatment. Response criteria were based on the effectiveness of the treatment, specifically the DAS28-ESR score.

### Pre-processing
Various methods for handling missing data were tested, including iterative imputation (MICE), k-nearest-neighbors-based imputation (KNN), mean, and median imputation. MICE was chosen for its accuracy in filling missing values.

### Model Design
Nested cross-validation with 5 iterations was used to avoid overfitting and data leakage. Hyperparameter tuning was performed using the optuna method, and feature selection was conducted using embedded feature selection in each predictor model.

## Results
### Baseline Sociodemographics and Clinical Factors
The filtered dataset contains 330 subjects with 43 features, including demographic and baseline clinical characteristics.

### Model Performances
Evaluation matrices, including accuracy, F1-score, precision, and AUC-ROC, were calculated for all models. Random Forest and XGBoost classifiers outperformed other models in predicting treatment response.

### Characteristics Importance
Feature importance analysis using SHAP values identified important predictors influencing the effectiveness of MTX therapy.

## Conclusion
This repository presents the results of applying various supervised machine learning models to predict treatment response in early RA patients. Random Forest and XGBoost classifiers perform better than other models, providing insights into important predictors of treatment effectiveness.


