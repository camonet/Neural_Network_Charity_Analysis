# Neural Network Charity Analysis
## Overview
The purpose of this analysis was to use deep learning to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Results: 

### Data Pre-processing
The variables in the dataset were: 
  - EIN and NAME—Identification columns
  - APPLICATION_TYPE—Alphabet Soup application type
  - AFFILIATION—Affiliated sector of industry
  - CLASSIFICATION—Government organization classification
  - USE_CASE—Use case for funding
  - ORGANIZATION—Organization type
  - STATUS—Active status
  - INCOME_AMT—Income classification
  - SPECIAL_CONSIDERATIONS—Special consideration for application
  - ASK_AMT—Funding amount requested
  - IS_SUCCESSFUL—Was the money used effectively
The IS_SUCCESSFUL variable was considered the target variable of the analysis. At this stage, we decided that EIN and NAME, the identification columns, were not necessary and were removed from the dataset. The rest of the variables were considered features.

###  Compiling, Training, and Evaluating the Model

   I selected 82 nerouns (3x the number of inputs) because the number of inputs was 20 for the first layer. After that i chose 30 neurons for the second layer. At the beginning i chose relu and the activation function and sigmoid as the outpid function. Sigmoid functions are optimized for binary classification systems. With this, i got these numbers: 
   <img width="646" alt="Screen Shot 2022-08-17 at 5 16 36 PM" src="https://user-images.githubusercontent.com/99444856/185253231-61cc2ade-5a9f-461a-bce1-2dce0d49f24f.png">
   
   Trying to increase the accuracy score was a losing battle, however. The steps I took to increase model performance are shown below for each of my three attempts. 
   - Attempt 1 (adding 2 hidden layers, changing APPLICATION_TYPE bins)
   <img width="646" alt="Screen Shot 2022-08-17 at 5 18 52 PM" src="https://user-images.githubusercontent.com/99444856/185253552-f416090e-ce03-45b2-9eac-9e950d45f7b3.png">
   
   - Attempt 2 (changing activation functions from relu to sigmoid, adding 2 hidden layers, dropping special_considerations and use_case columns, reducing epochs)
  <img width="646" alt="Screen Shot 2022-08-17 at 5 19 47 PM" src="https://user-images.githubusercontent.com/99444856/185253656-e424eaf5-70ab-4185-9302-c654fa055ab6.png">
  
  - Attempt 3 (back to regular dataset, changed activation functions to tanh, decreased neurons, change class bin size)
  <img width="646" alt="Screen Shot 2022-08-17 at 5 20 31 PM" src="https://user-images.githubusercontent.com/99444856/185253732-e0a42433-2235-414a-8115-479a78302465.png">

## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation
  The overall results from this analysis are that this model is not an exceptional predictor at determining success. Another model that performs binary classification accurately with good interpretability is the RandomForestClassifier model.





