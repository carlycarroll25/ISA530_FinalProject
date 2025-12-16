# Quantifying the Predictive Power of Biological and Environmental Factors in Adult Health Outcomes

## Overview
This project applies machine learning and statistical modeling techniques to examine how biological conditions and environmental factors contribute to adult health outcomes using a genetically informed twin design. Leveraging data from the Midlife in the United States (MIDUS) twin sample, the analysis isolates shared genetic and early life influences, while evaluating how environmental and behavioral factors drive health divergence across adulthood. The project integrates unsupervised learning, supervised prediction, and longitudinal modeling to provide a comprehensive assessment of health variation over time.

## Project Structure

### Data
This project uses a cleaned subset of the Midlife in the United States (MIDUS) study restricted to twin pairs. The datasets included here are processed versions of the original MIDUS twin data, prepared for cross sectional, longitudinal, and within twin pair analyses.
- **`MIDUS_twins_wide.csv`**: Wide format dataset with one row per individual, used for supervised learning and cross sectional analyses
- **`MIDUS_twins_long.csv`**: Long format dataset with repeated observations across MIDUS waves, used for longitudinal mixed effects modeling
- **`MIDUS_twins_diffs.csv`**: Within twin pair difference dataset used to isolate environmental and behavioral divergence while controlling for shared genetics

### Files
- **`Data Preprocessing.ipynb`**: Cleans and prepares MIDUS twin data, constructs wide, long, and within pair difference datasets, and standardizes variables
- **`Exploratory Data Analysis.ipynb`**: Performs descriptive analysis of self rated health, biological conditions, and environmental factors
- **`Unsupervised Learning.ipynb`**: Implements PCA and K-means clustering on biological and environmental feature sets with twin pair comparisons
- **`Supervised Learning.ipynb`**: Applies supervised models including Support Vector Machines, logistic regression, and gradient boosted decision trees
- **`Longitudinal Analysis.ipynb`**: Estimates mixed-effects longitudinal models to assess health changes and variance decomposition across MIDUS waves

### Reports
- **`ISA530_FinalProjectReport.pdf`**: A comprehensive academic report detailing background, methodology, analysis, results, and conclusions
- **`ISA530_FinalProjectPresentation.pdf`**: A presentation summarizing the project motivation, modeling approach, and key findings

## Methodology
The project followed these main steps:
1. **Data Preprocessing**: Cleaned and reshaped MIDUS twin data into wide, long, and within-pair difference formats and standardized predictors
2. **Exploratory Data Analysis**: Examined distributions and relationships among health, biological, and environmental variables
3. **Unsupervised Learning**: Applied PCA and clustering to identify structure and similarity in biological and environmental features
4. **Supervised Learning**: Used classification models to predict self rated health at both the population and within pair levels
5. **Longitudinal Modeling**: Implemented mixed effects models to evaluate health trajectories and variance components over time

## Key Results
- **Unsupervised Analysis**: Biological features formed tighter clusters with greater twin similarity, while environmental features exhibited higher dispersion and divergence
- **Support Vector Machine**: Within pair prediction of health differences achieved modest accuracy (≈0.53), reflecting strong shared baselines and subtle divergence
- **Logistic Regression**: Population level SRH prediction achieved an AUC of approximately 0.78, with both biological and environmental predictors showing meaningful effects
- **Gradient Boosted Trees**: Performance comparable to logistic regression, with age, BMI, education, and depressive symptoms emerging as key predictors
- **Longitudinal Modeling**: Family and individual level effects explained a substantial portion of health variance, while environmental predictors remained significant across waves

## Installation
To run this project locally, ensure the following Python libraries are installed:

- `os`
- `typing`
- `numpy`
- `pandas`
- `pyreadstat`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `statsmodels`
- `scipy`
- `IPython`
- `jupyter`
