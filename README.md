# H1N1 FLU VACCINATION PREDICTION: A Machine Learning Project
## Project Overview

In this project, we want to use data from the National Flu Survey (NHFS 2009) to predict whether or not respondents got the H1N1 vaccine. It is important to understand past vaccination patterns in order to understand those of more recent pandemics, such as COVID-19. The most influential factors determining vaccination status are found to be Doctor Recommendation of H1N1 vaccine, Health Insurance, opinion of H1N1 Vaccine effectiveness, opinion of H1N1 risk. We used six machine learning models to make the predictions according to analysis results. We used Decision Tree Classifier, Logistic Regression, Random Forest, K-Nearest Neighborhood Classifier, Gradient Boosting Classifier, and XG Boosting Classifier. The Gradient Boosting Classifier yielded the best accuracy and precision score.

## Data Overview

This data comes from a NHFS National Flu Survey from 2009, which inquires about whether or not people received the seasonal flu and/or the H1N1 flu vaccination, as well as their demographic, behavioral, and health factors. There are 26,000 respondents to this survey. In this project we chose H1N1 vaccination rate as our target variable. We used all features in the survey, and filled missing values using the Iterative Imputer.


## Methodology

We wanted to use a variety of different models so as to find the most accurate model. Because there are many different hyperparameters for each model and we did not know the optimal combinations, we used GridSearrchCV to find the best combinations for each model. We specified class weight to be balanced in order to address the class imbalance issue for our models, whenever possible. We also analyzed the accuracy score, precision score, fl score, and roc-auc curve for each model. We also compared the different roc-auc curves of each model, to choose the final model. Additionally, we looked closely at the confusion matrix to see whether or not we were minimizing false positives. Gradient Boosting Classifier gave us the best accuracy and precision scores, so we chose it to be our final model.


## Project Results

The Gradient Boosting model has the highest overall scores of all the models done so far, and also does the best job of minimizing the false positives. This  model did not overfit to the training set, we got similar AUC, precision and accuracy scores for the holdout set. Because the model does a good job of minimizing the false positive rate on the hold out data, we are fairly confident that it will generalize well to unseen data and will accurately help public health offials determine the people who didn't get the vaccine. 

We also looked into feature importances to understand the relationship between the features and vaccination behavior. We saw that the demographic and behavioral features are not that important compared to health related factors and opinions. The doctor recommendation, health insurance, opinion of vaccine efficiency, and opinion of H1N1 risk are the top important factors in determining people's vaccination status.


## Conclusion

We recommend that public health officials at the American Public Health Association (APHA) communicate to doctors the importance of recommending to patients that they get the H1N1 vaccine. We also recommend that they find a way to make the vaccine accesible to people regardless of health insurance status. Additionally, because opinion on H1N1 vaccine effectiveness and H1N1 risk to health are highly influential in determining vaccination status, we recommend that the APHA make educational outreach a priority. Our analysis might not fully resolve the goal of predicting H1N1 vaccination status because we were not able to fully rule out false negatives, or people who we predicted as not getting vaccinated but actually did get the vaccine. Additionally, there may be other factors at play which were not tapped into by this survey's questions which could also paly a role in vaccination prediction. 

## Next Steps

For our next steps, we would like to look at more recent flu survey data, so as to get the most recent results. We would also like to do more feature engineering to improve accuracy. Lastly, since we chose to focus only on predicting H1N1 vaccination status, we would like to focus in the future on predicting seasonal flu vaccine status.


## Repository Navigation

### Data:
- https://www.drivendata.org/competitions/66/flu-shot-learning/page/213/


### Notebooks
- Final notebook: https://github.com/emykes/Flu_Vaccination_ML/blob/main/Project3_Main_Notebook.ipynb
- Modeling iterations: https://github.com/emykes/Flu_Vaccination_ML/blob/main/Project3_model_iterations.ipynb

### Presentation



### Team Members

- Brooke Smyth: https://github.com/brooke57
- Emine Kesici: https://github.com/emykes
- Tamiru B. Denka: https://github.com/Tamiru3
