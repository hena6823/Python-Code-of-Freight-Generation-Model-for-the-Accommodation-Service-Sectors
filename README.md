Freight Generation Model for the Accommodation Service Sector

Overview

This repository contains the Python code used to develop and evaluate the Freight Generation Models for the Accommodation Service Sector in Addis Ababa, Ethiopia.

The analysis forms part of an MSc thesis on urban freight generation modelling.
The objective is to estimate annual Freight Production (FP) and Freight Attraction (FA) using establishment-level characteristics.

The analysis applies Ordinary Least Squares (OLS) multiple regression to identify the relationship between freight generation and selected establishment characteristics.

Study Sector

The model focuses on the Accommodation Service Sector (ISIC Code 55) in Addis Ababa.

The dataset contains 277 accommodation establishments.
The analysis considers both outbound freight production and inbound freight attraction.

Variables

Dependent Variables

Freight Production (FP): Quantity of outbound freight in ton/year.

Freight Attraction (FA): Quantity of inbound freight in ton/year.

Explanatory Variables

The models use three establishment-level variables:

Number of Years in Operation

Number of Employees

Gross Floor Area (m²)

These variables were selected because they represent important operational and physical characteristics of accommodation establishments.

Methodology

The Python workflow includes:

Importing and inspecting the establishment-level dataset.

Examining descriptive statistics and data structure.

Checking for missing and duplicated observations.

Exploring the distributions of the variables through graphical analysis.

Separating the explanatory and dependent variables.

Dividing the data into training and hold-out test sets.

Estimating linear regression models using scikit-learn.

Estimating OLS models using statsmodels.

Calculating regression coefficients and statistical significance.

Evaluating model performance using MAE, RMSE, and R².

For both FP and FA, 80% of the observations were used for model estimation and 20% were reserved for hold-out testing.

For the Accommodation sector, this resulted in:

Training observations: 221

Hold-out test observations: 56

Model Specification

The general form of the regression model is:

Y = β₀ + β₁X₁ + β₂X₂ + β₃X₃ + ε

where:

Y = Freight Production or Freight Attraction

β₀ = intercept

X₁ = Number of Years in Operation

X₂ = Number of Employees

X₃ = Gross Floor Area (m²)

ε = error term

Freight Production Model

The estimated Accommodation FP equation is:

FP = −28.950 − 1.532(Years) + 4.780(Employees) + 0.085(GFA)

Freight Attraction Model

The estimated Accommodation FA equation is:

FA = −40.188 − 1.547(Years) + 0.950(Employees) + 0.077(GFA)

Model Performance

The Accommodation models demonstrate strong explanatory and predictive performance.

Freight Production

R²: approximately 0.990

MAE: 49.74 ton/year

RMSE: 62.79 ton/year

Freight Attraction

R²: approximately 0.992

MAE: 29.97 ton/year

RMSE: 38.57 ton/year

The results indicate that the selected establishment characteristics explain a large proportion of the observed variation in freight generation within the Accommodation sector.

Statistical Analysis

The statsmodels OLS implementation is used to obtain:

Regression coefficients

Standard errors

t-statistics

p-values

R² and adjusted R²

F-statistics

Confidence intervals

Full regression summaries

The analysis also reports the statistical significance of the individual explanatory variables.

For the Freight Production model, Number of Employees and Gross Floor Area show statistically significant relationships with freight production, while Number of Years in Operation is not statistically significant at the conventional 5% level.

Python Libraries

The analysis uses Python-based statistical and data-analysis tools, including:

pandas
numpy
matplotlib
seaborn
scikit-learn
statsmodels
scipy

The principal modelling procedures use LinearRegression from scikit-learn and OLS regression from statsmodels.
    
Reproducibility

To reproduce the analysis, open the Jupyter Notebook and run the cells sequentially.

The original analysis was developed using establishment-level accommodation survey data from Addis Ababa.
If the underlying dataset is not publicly available, users should not expect to reproduce the numerical results without access to the original data.

Data Availability

The Python code is made publicly available to promote transparency and reproducibility of the research.

The availability of the underlying establishment-level dataset depends on data confidentiality and the conditions under which the survey data were collected.
Where the raw data cannot be publicly released, the code can still be used to document the modelling procedure and analytical workflow.

Research Context

This code supports research on urban freight generation modelling in Addis Ababa, Ethiopia.

The analysis contributes to the development of establishment-based freight generation models for service-sector establishments, with particular attention to the relationship between freight demand and establishment characteristics.

The Accommodation model presented here forms part of a broader multi-sector freight generation study covering selected service sectors in Addis Ababa.

Citation

If you use or adapt this code in academic research, please cite the associated MSc thesis.

Suggested citation:

Henock. Freight Generation Modelling for Selected Service Sectors in Addis Ababa, Ethiopia. MSc Thesis.

The final bibliographic details should be updated once the thesis has been formally submitted or published.

Author

Henock
MSc Researcher
Addis Ababa, Ethiopia

Disclaimer

This repository contains research code developed for academic purposes.
The models are calibrated for the Accommodation Service Sector in Addis Ababa and should not be assumed to be directly transferable to other cities or sectors without appropriate validation and, where necessary, recalibration.
