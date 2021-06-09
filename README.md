# Endogeneity in statistical inference and forecasting
Project created for *Simulations and Forecasting* classes at WNE UW

Language:
 * Polish - classes, notebook, report

Semester: IV (MA studies)

## About
The main objective of this project was to analyze identification problems in statistical inference and forecasting based on linear regression model. The approach was to generate the data (1 000 000 observations) according to defined Data Generation Process (DGP) and estimate some models. The idea was to analyze behavoir of the regression coefficients and predictions depending on explanatory variables variables set. The DGP contained variables such as mediators (positive and negative), confounders, instrumental and mediated. After regression results analysis the Monte Carlo simulation was performed. The simulation was about DGP structural parameters sampling (1 000 times) to see if our conclusions about forecasting are generalisable. We also tried to answerar the question: Can standard OLS diagnostic help to find the right model? RMSE was the prediction metric.

Findings:
 * standad diagnostics doese not guarantee finding the right model
 * sign of the mediator does not matter (assuming that mediator has positive impact on dependent variable) in terms of predictions
 * if ommited variable is positively correlated with explanatory and dependent variable then the explanatory variable becomes endogenous and overestimated (ommited variable bias)
 * if ommited variable is negatively correlated with explanatory variable and positively correlated with dependent variable then the explanatory becomes endogenous and underestimated (ommited variable bias)
 * ommitted variable bias can be solved with instrumental variables with unilateral influence on the endogenous variable and model residuals and uncorrelated with another explanatory variables
 * instrumental variable estimator is consistent but not effective (OLS estimator is biased but has lower standard errors)
 * there can be a trade-off: the unbiased model may not be the best for predictions
 * without theoretical analysis it can be impossible to find the right model specification, but it is easier to find the best model for predictions

## Repository description
 - Prognozowanie_i_symulacje.ipynb - Jupyter Notebook with Python code and comments
 - dgp_v2.png - Data Generation Process diagram
 - report.pdf - project report 
 - wyniki_symulacji.csv - simulation results (1 000 draws, 1 000 000 observations each)

## Technologies
 - Python (numpy, pandas, seaborn, statsmodels, scipy, stargazer)
 - Jupyter Notebook
 - Microsoft Word :)

## Authors
 - Maciej Odziemczyk
 - Karolina Stępień

## Note
The whole idea was based on the Judea Pearl's causality theory, I encourage you to read more about in the "CAUSALITY Models. Reasoning and Inference" Cambridge Univeristy Press (2000/2009).
