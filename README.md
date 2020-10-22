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
The overall goal for our group was to create a model that has the lowest chance of making a type two error or give results that are false negative.  In this case that would mean the model predicts a person will cancel their contract with SyriaTel but do not do so. 

## Data
The [project data](https://www.kaggle.com/becksddf/churn-in-telecoms-dataset) came from Kaggle.com.  It contains data on phoneplans from over 3300 customers detailing information specific to billing of the customer, information specific to the customer, and information detailing each customers plan, the number of times a customer has called customer service, and finally whether or not the customer has cancelled their contract which is represented by churn in the dataset.  The data can most esily be uploaded to a notebook using the Pandas read .csv method. 

## Data Preperation/Exploration
During the implementation of the first simple model churn was chosen as the target feature of our models since the goal was to find how the features would interact to show why a person might cancel their contract.  This feature was separated from the rest and the entirety of the features were used to implement a train-test split to be applied to the models.

### Linear Regression Model
A linear regression model was used for the first simple model
    
