# SyriaTel Customer Churn Project

This project analyzes what might cause someone to cancel their service to SyriaTel and predict who might drop their service in the near future.

## Directory Structure

### [Notebooks](https://github.com/oklena/SyriaTel_Customer_Churn/tree/master/notebooks)
This folder contains jupyter notebooks with exploratory data analyses and our final report notebook.

### [Reports]
This folder contains a pdf of our slideshow presentation, and images used in the finalized presentation of the data.

### [Data](https://github.com/oklena/SyriaTel_Customer_Churn/tree/master/data)
This folder conatains all relevant documentation for the data used in this repo.

## Background
The overall goal for our group was to create a model that has the lowest chance of making a type two error or give results that are false negative.  In this case that would mean the model predicts a person will cancel their contract with SyriaTel but do not do so. 

## Data
The [project data](https://www.kaggle.com/becksddf/churn-in-telecoms-dataset) came from Kaggle.com.  It contains data on phoneplans from over 3300 customers detailing information specific to billing of the customer, information specific to the customer, and information detailing each customers plan, the number of times a customer has called customer service, wnd finally whether or not the customer has cancelled their contract.  The data can most esily be uploaded to a notebook using the Pandas read .csv method. 

## Data Preperation/Exploration
The phone number column and the categorical columns in the Customer Churn data frame were separated and one  
    
