# SyriaTel Customer Churn Project

This project analyzes what might cause someone to cancel their service to SyriaTel and predict who might drop their service in the near future.

## Directory Structure

### [Notebooks](https://github.com/oklena/SyriaTel_Customer_Churn/tree/master/notebooks)
This folder contains jupyter notebooks with exploratory data analyses and our final report notebook.

### [Reports]
This folder contains a pdf of our slideshow presentation, and images used in the finalized presentation of the data.

### [Data](https://github.com/oklena/SyriaTel_Customer_Churn/tree/master/data)
This folder conatains all relevant documentation for the data used in this repo.

## Data
The data for this project came from <https://www.kaggle.com/becksddf/churn-in-telecoms-dataset>.  It contains data on phoneplans from over 3300 customers detailing information specific to billing of the customer, information specific to the customer, and information detailing each customers plan, the number of times a customer has called customer service, wnd finally whether or not the customer has cancelled their contract.  The categorical data was dummied the numerical data was scaled, and the SMOTE method was used to better balance the data classes.  There were several models used for this report including linear regression, random forests, and descision tree classifier.
    
