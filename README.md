# Neural Network Model Analysis

## Overview

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. This analysis used the features in the provided dataset to create a binary classifier that predicted whether applicants were successful if funded by Alphabet Soup.

The Alphabet Soup’s business team, provided a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

* **EIN** and **NAME**—Identification columns
* **APPLICATION_TYPE**—Alphabet Soup application type
* **AFFILIATION**—Affiliated sector of industry
* **CLASSIFICATION**—Government organization classification
* **USE_CASE**—Use case for funding
* **ORGANIZATION**—Organization type
* **STATUS**—Active status
* **INCOME_AMT**—Income classification
* **SPECIAL_CONSIDERATIONS**—Special considerations for application
* **ASK_AMT**—Funding amount requested
* **IS_SUCCESSFUL**—Was the money used effectively

## Results

1. **Preprocessing:** 
   *  Google Colab was used for this analysis. 
   * The identified target variables was is_successful
   * The featured variables were primarily application_type and classification, but all other fields were included aside from
     ein and name due to these two fields being neither a feature nor a target variable of interest.
   * Categorical variables were converted to numeric values using Pandas get_dummies. 
   * The data was then split into training and testing datasets, and the features were scaled using StandardScaler.

2. **Compiling, Training, and Evaluation the Model:**
   *  Two hidden layers were chosen; the first containing 150 nodes and the second containing 100 nodes
   *  Two activation functions were used and both were relu
   *  The output layer was sigmoid
   *  The model was trained with 100 epochs utilizing the training dataset. 

## Model Summary

The neural network model used in this analysis did not achieve ideal performance standards for the ability to satisfactorily predict success of charity funding applications. The model achieved an accuracy of approximately 73% and a loss of 57% in spite of best efforts to use other activation functions, hidden layers and nodes. My recommendation would be to utilize a different model entirely for improved accuracy and prediction performance going forward. 

<p align="center">
  <img width="600" height="150" src="https://github.com/SEBraun1/deep-learning-challenge/blob/2f0f7c2ffcf4282f6352107577a3143bdfeccb39/modelresults.PNG">
</p>
