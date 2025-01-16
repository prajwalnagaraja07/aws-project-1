# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Prajwal Nagaraja

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
Firstly, Kaggle competitions do not allow negative predictions. Therefore, it is essential to ensure all predictions are non-negative by setting any negative values to 0. Additionally, the data must always be submitted in the correct format, as outlined in the "sampleSubmission.csv" file.

### What was the top ranked model that performed?
In the third stage of the project, we focused on enhancing the model's performance by engineering new features and fine-tuning key hyperparameters. During this phase, the Weighted Ensemble L3 model emerged as the top-performing model, effectively leveraging the improvements made to deliver superior results.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
The exploratory analysis revealed that the time variable was not in its optimal format, as it was categorized as an object. To address this, we converted it to a datetime format and further broke it down into separate components, including month, day, day of the week, and time, for more granular analysis.

### How much better did your model preform after adding additional features and why do you think that is?
The model's performance improved significantly, with the score dropping from approximately **1.8** to **0.62** after incorporating temporal variables. This highlights the critical role of time as a variable in demand forecasting and underscores its necessity in the model. This conclusion is logical, given that the data pertains to a time series, where temporal patterns are inherently influential.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
By fine-tuning certain hyperparameters, the model's performance improved noticeably. Although the change was relatively small, even minor improvements are valuable in competitive settings. The model's score decreased from approximately **0.62** to **0.49**, reflecting a meaningful enhancement in accuracy.

### If you were given more time with this dataset, where do you think you would spend more time?
I would definitely dedicate more time to thoroughly exploring the data and creating additional variables for the model. This is because the variables had a significant impact on the model's performance, making feature engineering a crucial area for further improvement.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|default|default|default|1.8|
|add_features|default|default|default|0.62|
|hpo|max_depth: 16|max_features: 0.77379	|max_samples: 0.91334	|0.49|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

![model_train_score](https://github.com/user-attachments/assets/be0cdf42-0655-4130-a2e2-8799b19a14df)


### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![model_test_score](https://github.com/user-attachments/assets/7f1cc8b9-de0b-4b8f-b31e-40646869a1e0)


## Summary
Overall, I was highly impressed with AutoGluon's performance on the data. Its ease of use allows us to quickly identify efficient models, enabling us to concentrate more on data quality, feature engineering, and hyperparameter optimization. 

Moving forward, the next steps would involve conducting a more in-depth exploration of the data using visualizations and statistical analysis. Following this, the focus should shift to identifying a specific model that delivers the best performance. Finally, the hyperparameters of that model can be fine-tuned to maximize its potential and aim for victory in the competition!