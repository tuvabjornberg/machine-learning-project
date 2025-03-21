# Predicting duration of New York taxi trip for 1DL034 Introduction to machinelearning

Run on datasets from the course's Kaggle page: https://www.kaggle.com/competitions/1dl034-project-vt25/data
* training_dataset.csv - the training set consists of 32,701,098 rows of data you need for training.
* evaluation_dataset.csv - the test dataset to evaluate the model performance. This may or may not include entries from training_dataset.csv. In this dataset, tpep_dropoff_datetime and duration columns are removed for obvious reasons.
* sample_submission.csv - a sample submission file in the correct format.
* taxi_zone_lookup.csv - a lookup table for zones (you may or may not need it, depending on how you plan to model your approach).


A predictor for predicting the duration of a taxi ride was made using a Random Forest regression model. The selection of the type of model was done by testing some of the most ”well known” models, those covered in this course, and selecting the one that performed best.

Before testing, the data was pruned to where most, if not all of the ”bad data” had been removed. This ensured that the algorithm can converge towards a realistic value without all the outliers worsening the predictions. This includes handling both missing and non-numerical data, as well as removing datapoints with unrealistic values.

The trained model completed predictions of the duration of a taxi trip with a RMSLE score of 0.26077 and with ≈ 79 seconds error from the actual trip.

The greatest impact of the predictions were the amount of data that was used when training the model. Despite using preprocessing methods, like normalization, bucketing or tuning hyperparameters, increasing the amount of data had the greatest impact.