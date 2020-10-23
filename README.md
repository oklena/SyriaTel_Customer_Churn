![SyriaTel Logo](https://github.com/oklena/SyriaTel_Customer_Churn/blob/master/reports/figures/SyriatelLogo.jpeg)

# SyriaTel Customer Churn Project

This project analyzes what might cause someone to cancel their service to SyriaTel and predict who might drop their service in the near future.

## Directory Structure

### [Notebooks](https://github.com/oklena/SyriaTel_Customer_Churn/tree/master/notebooks)
This folder contains jupyter notebooks with exploratory data analyses and our final report notebook.

### [Reports](https://github.com/oklena/SyriaTel_Customer_Churn/tree/master/reports/figures)
This folder contains a pdf of our slideshow presentation, and images used in the finalized presentation of the data.

### [Data](https://github.com/oklena/SyriaTel_Customer_Churn/tree/master/data)
This folder conatains all relevant documentation for the data used in this repo.

### [SRC](https://github.com/oklena/SyriaTel_Customer_Churn/tree/master/src)
This folder contains the source code for created functions for use during this project.

## Background
The overall goal for our group was to create a model that has the lowest F1 score showing the least number of both type one and type two errors. In other words we attempted to make a model that would help identify the errors in SyriaTel's predictions of whether a customer might stay but then doesn't or weather a customer might leave but stays.

## Data
The [project data](https://www.kaggle.com/becksddf/churn-in-telecoms-dataset) came from Kaggle.com.  It contains data on phoneplans from over 3300 customers detailing information specific to billing of the customer, information specific to the customer, information detailing each customers phone plan, the number of times a customer has called customer service, and finally whether or not the customer has cancelled their contract which is represented by churn in the dataset.  The data can most esily be uploaded to a notebook using the Pandas read .csv method. 

## Data Preperation/Exploration
When preparing the data the categorical features were placed in a separate datafram and one-hot-encoded it was then added to the numerical features after they had been scaled to prevent over penalization from our models.  During the implementation of the first simple model, churn was chosen as the target feature of our models since the goal was to find how the features would interact to show why a person might cancel their contract.  This feature was separated from the rest and placed in a variable and the entirety of the features were used to implement a train-test split to be applied to the models.  

### Logistic Regression Model
Logistic regression was used as our first simple model.  It is designed to compare the conditional probabilities of many independent features and then uses those calculations to find the total conditional probability of the target feature. The linear regression model used hyperperameter tuning to reach an F1 score of .485.

![first_log](https://github.com/oklena/SyriaTel_Customer_Churn/blob/master/reports/figures/first_log.jpg)

### K-Nearest Neighbors Model
The K-nearest neighbors model uses a distance metric to identify if a new data point will be labeled the same as features near its predicted location by averaging the number of points with each label and giving the new point the label of the label with the highest mean. For this model the SMOTE function was used to balance the sample data set and the target data set and help prevent bias between the datasets.  The KNN model F1 score was a .873 but it was over fit to the training data.

![first_knn](https://github.com/oklena/SyriaTel_Customer_Churn/blob/master/reports/figures/first_knn.jpg
)
### Random Forest Classifier
A random forest classifier uses a discrete function to identify how to give wieight to one posibility over another until each possibility has been considered and weighed leaving a clear outcome.  SMOTE was also applied to the data of the Random Forest Model to balance the difference between the sample data set and the target data set.  This model was the final model for the project and had a high mean F1 score of .775.

![second_rand](https://github.com/oklena/SyriaTel_Customer_Churn/blob/master/reports/figures/second_knn.jpg)

## Evaluation
The metric used to evaluate each model was the F1 score or the harmonic mean of the recall and precision scores.  These are the measueres of the number of false negatives and true negatives.  The method for calculating the F1 score causes the number to be much lower if there are too many of either error when the average is taken, for this reason it is a good measure for the overall performance of the models.  The Logistic Regression model had a high false positive metric at 651 and low false negetive at 90 showing a low performance in the f1 score.  The K-nearest neighbors model has a similar issue and an even lower F1 score.  However, the final model has a high f1 score and a good measure between the recall and precision metrics.
    
#### Title banner from logolynx.com
