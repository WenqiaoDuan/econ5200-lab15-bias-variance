# econ5200-lab15-bias-variance
# Bias, Variance and an Unbiased Cross-Validation Score

## Objective

I wanted to understand how model complexity affects prediction error and how cross-validation estimates model performance.

## Methodology

- I used 80 simulated data points and tested polynomial models from degree 1 to 12 using cross-validation.
- I selected the degree with the lowest CV error.
- I tested the selected model on 20,000 new data points to measure its true error.
- I used nested cross-validation to estimate the error of the model selection process.
- I used simulation to separate prediction error into bias squared, variance, and noise.
- I wrote my own k-fold cross-validation function for scikit-learn models and compared its results with the lab.

## Key Findings

- Degree 5 had the lowest CV error of 0.1853.
- The true error was 0.2330, higher than the reported CV error.
- Nested CV estimated an error of 0.1910.
- The noise level was 0.2025.
- My k-fold function gave an MSE of 0.1921 for degree 5 using 10 folds.

I learned that choosing a model based on the lowest CV error can make its performance look better than it really is. Nested CV helps reduce this selection bias, but random variation can still affect the results. I also learned that increasing model complexity does not always improve predictions.
