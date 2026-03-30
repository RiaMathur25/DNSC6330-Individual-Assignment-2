# COMPAS Analysis

## Individual Homework 2

## A) Purpose of the Analysis

This repository contains a transparency and fairness assessment of a Gradient-Boosted Tree model trained on the Broward County COMPAS dataset. The notebook evaluates how the model predicts two-year recidivism outcomes and examines whether prediction errors differ across demographic groups using post-hoc explainability methods.

The Python notebook implements the following analytical workflow:

1. Data loading from ProPublica’s public COMPAS dataset repository
2. Data cleaning and preprocessing: filtering rules, variable selection, and encoding of categorical features
3. Gradient-Boosted Tree model development to predict two-year recidivism outcomes
4. Model diagnostics: confusion matrix with accuracy, precision, recall, false positive rate (FPR), and false negative rate (FNR)
5. Fairness analysis: subgroup comparison of FPR and FNR across racial groups
6. Global explainability analysis using SHAP summary (beeswarm) plots
7. Local explainability analysis using SHAP waterfall plots for selected individuals
8. Comparison of explanation methods using LIME local feature attributions
9. Counterfactual recourse analysis using DiCE to identify feature changes that alter predicted outcomes



The results show that variables such as age, priors\_count, and decile\_score strongly influence predicted recidivism risk. Subgroup evaluation indicates differences in false positive rates across racial groups, illustrating that transparency analysis can help identify potential disparities in model behaviour.

## B) Python Libraries Used

|Library|Purpose|
|-|-|
|pandas|Data loading, filtering, groupby operations|
|numpy|Numerical operations and transformations|
|matplotlib|Visualization of model outputs|
|seaborn|Statistical plotting support|
|scikit-learn|Gradient Boosted Tree model and evaluation metrics|
|shap|Global and local feature attribution analysis|
|lime|Local surrogate explanations|
|dice-ml|Counterfactual explanation generation|

## C) Instructions for Reproducing the Results (Google Colab)

1. Open Google Colab
2. Upload Individual\_Assignment\_2.ipynb
3. Run all cells using Runtime → Run all

