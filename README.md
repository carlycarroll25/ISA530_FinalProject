# Quantifying the Predictive Power of Biological and Environmental Factors in Adult Health Outcomes

## Overview
This project applies machine learning and statistical modeling techniques to examine how biological conditions and environmental factors contribute to adult health outcomes using a genetically informed twin design. Leveraging data from the Midlife in the United States (MIDUS) twin sample, the analysis isolates shared genetic and early life influences, while evaluating how environmental and behavioral factors drive health divergence across adulthood. The project integrates unsupervised learning, supervised prediction, and longitudinal modeling to provide a comprehensive assessment of health variation over time.

## Project Structure

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
To set up this project locally, follow these steps:
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/YourUsername/YourRepositoryName.git
   cd YourRepositoryName
   ```
2. **Install Required Packages**:
```bash
   pip install -r requirements.txt
```
4. **Upload Data**:
   - Place MIDUS twin CSV files in the project directory
   - Ensure file names match those referenced in the notebooks
5. **Run the Project**: Execute notebooks sequentially, starting with Exploratory Data Analysis.ipynb
