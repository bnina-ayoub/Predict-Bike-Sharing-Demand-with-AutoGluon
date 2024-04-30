# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Ayoub Bnina

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
When trying to submit predictions, I realized that AutoGluon's output wasn't in the format required by the Kaggle competition. The leaderboard likely expects a specific format, such as a CSV file with a "prediction" column containing the predicted bike sharing demand for each test data point. You would need to post-process AutoGluon's output to match this format.

### What was the top ranked model that performed?
The top ranked model after the initial training was most likely the "WeightedEnsemble_L3" model. It has the highest score_val (-35.152490) amongst all the models in the initial training run.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
During EDA, I encountered a situation where the datetime column wasn't visualized in the histogram plots. This have indicated that the datetime column had a different data type (e.g., object type for strings) compared to numerical features typically used in histograms.

Since the datetime held potentially valuable information about time-based patterns, this invisibility in histograms prompted me to explore ways to extract meaningful features from it. For that I parsed the datetime column into date representation suitable for further analysis.

### How much better did your model preform after adding additional features and why do you think that is?
The model performance likely improved after adding new features because these features captured more information relevant to predicting bike sharing demand. For instance, including features like month, year and day of week could help the model learn seasonal trends and weekly patterns in demand.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
In the leaderboard, the score_val of the top models after hpo (hyperparameter tuning) are better than those before hpo, I have increased the training time, as well as setting the hyperparameter to auto based on what I found in the documentation.

### If you were given more time with this dataset, where do you think you would spend more time?
If I were given more time with the dataset I would spend it in feature engineering by creating even more features based on the existing ones or try feature selection techniques to identify the most important features.
also I would try ensemble methods by combining predictions from multiple models to potentially achieve better results.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.

![ModelsTable.png](img/ModelsTable.png.png)

### Create a line plot showing the top model score for the three (or more) training runs during the project.

![training-run.png](cd0385-project-starter/project/img/training-run.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![kaggle-score.png](cd0385-project-starter/project/img/kaggle-score.png)

## Summary
In summary, I followed a machine learning pipeline for predicting bike sharing demand using AutoGluon. I started with initial training, then performed exploratory data analysis to create new features, followed by hyperparameter tuning to improve the model's performance. This report provides a documented record of the process and the results achieved at each stage.
