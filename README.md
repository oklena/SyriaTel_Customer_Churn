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
The [project data](https://www.kaggle.com/becksddf/churn-in-telecoms-dataset) came from Kaggle.com.  It contains data on phoneplans from over 3300 customers detailing information specific to the customer, information specific to billing of the customer, information detailing each customers phone plan, the number of times a customer has called customer service, and whether or not the customer has cancelled their contract which is represented by churn in the dataset.  The data can most esily be uploaded to a notebook using the Pandas read .csv method. 

## Data Preperation/Exploration
When preparing the data the categorical features were placed in a separate dataframe and one-hot-encoded. It was then added to the numerical features after they had been scaled to prevent over penalization from our models.  During the implementation of the first simple model, churn was chosen as the target feature of our models since the goal was to find how the features would interact to predict both types of error.  This feature was separated from the rest and placed in a variable and the entirety of the features were used to implement a train-test split to be applied to the models.  

The metric used to evaluate each model was the F1 score or the harmonic mean of the recall and precision scores.  These number are represented by the upper right square, the false positive, and the lower left square, the false negetive when combined and averaged against the number of true positives.  These two metirics are then used to calculate the f1 score.  The method for calculating the F1 score causes the number to be much lower if there are too many of either error when the average is taken, for this reason it is a good measure for the overall performance of the models.

### Logistic Regression Model
Logistic regression was used as our first simple model.  It is designed to compare the conditional probabilities of many independent features and then uses those calculations to find the total conditional probability of the target feature. The first linear model represented by the first confusion matix shown below had a mean f1 score of .351. The second linear regression model represented by the lower of the two confusion matrices had a lower f1 score but changed some the functions features to reach a mean F1 score of .416 though the precision and recall scores were not as balanced.

![first_log](https://github.com/oklena/SyriaTel_Customer_Churn/blob/master/reports/figures/first_log.jpg)
![second_log](https://github.com/oklena/SyriaTel_Customer_Churn/blob/master/reports/figures/second_log.jpg)

### K-Nearest Neighbors Model
The K-nearest neighbors model uses a distance metric to identify if a new data point will be labeled the same as features near its predicted location by averaging the number of features with each label and giving the new point the label of the features with the highest mean.  The first KNN model returned a mean f1 score of .170 due to the extremely high false positive count in the output from the function.  For the second KNN model the SMOTE function was used to balance the sample data and the target data set to help prevent bias between the datasets this gave it a mean F1 score of .3 and it was under fit to the training data even though the two error calculations were more balanced.

![first_knn](https://github.com/oklena/SyriaTel_Customer_Churn/blob/master/reports/figures/first_knn.jpg
)
![second_knn](https://github.com/oklena/SyriaTel_Customer_Churn/blob/master/reports/figures/second_knn.jpg)

### Random Forest Classifier
A random forest classifier uses a discrete function to identify how to give weight to one posibility over another until each possibility has been considered and weighed leaving a clear outcome. The first random forest model has an f1 core of zero due to the fact the model could not predict which people would drop their contracts as represented by the lower left square.  The second model used hyperperameter tuning and SMOTE to the data of the Random Forest Model to get a much more blanced return from the model for the false positives and true negetives.  This model was the final model for the project and had a mean F1 score of .775.

![first_rand](https://github.com/oklena/SyriaTel_Customer_Churn/blob/master/reports/figures/first_rand.jpg)
![second_rand](https://github.com/oklena/SyriaTel_Customer_Churn/blob/master/reports/figures/second_rand.jpg)

## Evaluation
  
  
  
#### Title banner from logolynx.com
