# NCAA Women's Tournament Outcome Prediction

A multiclass machine-learning analysis examining whether regular-season performance can predict how far a team advances in the NCAA Division I Women's Basketball Tournament.

**Tools:** R, tidyverse, tidymodels, ggplot2, Jupyter Notebook

[View the complete analysis](NCAA_Tournament_Outcome_Prediction.ipynb)

## Research Question

Can conference win percentage, regional win percentage, and conference rank predict a team's tournament outcome?

## Dataset

The original dataset contains **2,092 tournament appearances from 1982–2018** and was published by the Diverse Data Hub using NCAA records.

[View the original dataset](https://raw.githubusercontent.com/diverse-data-hub/diversedata/refs/heads/main/data-clean/womensmarchmadness.csv)

## Method

- Selected three predictors: conference win percentage, regional win percentage, and conference rank
- Removed observations with missing values in the selected variables
- Converted tournament finish into an ordered outcome with eight possible stages
- Used a stratified **75/25 training-test split**
- Standardized numeric predictors
- Tuned a K-nearest neighbours classifier using **five-fold cross-validation**
- Evaluated the final model using test accuracy and a confusion matrix

## Results

- Best-performing value: **K = 21**
- Cross-validation accuracy: approximately **43.1%**
- Held-out test accuracy: approximately **45.8%**
- The confusion matrix showed that the model performed better on common early-round outcomes than on rare late-round outcomes

The results suggest that the selected regular-season statistics contain some predictive information, but they do not fully explain tournament performance.

## Skills Demonstrated

- Data cleaning and transformation
- Exploratory data analysis
- Data visualization with ggplot2
- Multiclass classification
- Feature standardization
- Cross-validation and hyperparameter tuning
- Model evaluation and interpretation
- Reproducible analysis in Jupyter Notebook

## Limitations

Tournament outcomes are highly imbalanced, with far fewer teams reaching the later rounds. The model also uses only three predictors, so factors such as tournament seed, injuries, schedule strength, and team-specific performance are not included. Results describe historical patterns and should not be interpreted as guaranteed predictions.

## Project Background

This analysis was originally completed as an individual project for **UBC DSCI 100: Introduction to Data Science**. This portfolio version removes course instructions and reorganizes my original analysis for easier review. The modelling choices, code, results, and conclusions remain based on my original work.

## Author

**Shyla Khullar**  
UBC Mathematics student pursuing a Statistics minor  
[LinkedIn](https://www.linkedin.com/in/shyla-khullar-a6a205247)
