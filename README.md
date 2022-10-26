# Neural_Network_Charity_Analysis

## Overview

In this challenge we should be able to develop a neural network to assist determining which organizations should be considered for funding from AlphabetSoupCharity. 

Using machine learning and neural networks, we’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns

APPLICATION_TYPE—Alphabet Soup application type

AFFILIATION—Affiliated sector of industry

CLASSIFICATION—Government organization classification

USE_CASE—Use case for funding

ORGANIZATION—Organization type

STATUS—Active status

INCOME_AMT—Income classification

SPECIAL_CONSIDERATIONS—Special consideration for application

ASK_AMT—Funding amount requested

IS_SUCCESSFUL—Was the money used effectively

## Results

**Preprocessing Data for a Neural Network Model**

- What variable(s) are considered the target(s) for your model?

*The target of IS_SUCCESSFUL is currently the only target for this model*
   

- What variable(s) are considered the feature(s) for your model?

*APPLICATION_TYPE*

*AFFILIATION* 

*CLASSIFICATION* 

*USE_CASE*

*ORGANIZATION*

*STATUS*

*INCOME_AMT*

*SPECIAL_CONSIDERATIONS*


- What variable(s) are neither targets nor features, and should be removed from the input data?

*EIN and NAME*

**Compiling, Training, and Evaluating the Model**

-How many neurons, layers, and activation functions did you select for your neural network model, and why?

In the initial attempt there were 2 layers with 80 and 30 neurons respectively (both "relu" type). Also the activation feature of "sigmoid" was used initially. 

-Were you able to achieve the target model performance (75%)? 

Unfortunately, the initial model was able to achieve an overall accuracy rating of 55% (average)

-What steps did you take to try and increase model performance?

In order to improve the performance of the model, there were developed 3 attemps with the following results:

***Attempt 1:***

-Dropped noisy data of ASK_AMT

-Layer 1: 80 neurons and type "tanh"

-Layer 2: 30 neurons and type "relu"

-Activation: sigmoid

-Accuracy: 55%


***Attemp 2:***

-Dropped noisy data of ASK_AMT

-Layer 1: 80 neurons and type "tanh"

-Layer 2: 50 neurons and type "relu"

-Layer 3: 30 neurons and type "sigmoid"

-Activation: relu

-Accuracy: 60%


***Attemp 3:***

-Dropped noisy data of ASK_AMT

-Layer 1: 100 neurons and type "sigmoid"

-Layer 2: 75 neurons and type "sigmoid"

-Layer 3: 50 neurons and type "relu"

-Layer 4: 25 neurons and type "relu"

-Activation: sigmoid

-Accuracy: 68%


## Summary:

As mentioned before the initial model did not achieve the level of performance required of 75% of accuracy, nevertheless through iterative design, the model was able to adjust and get better performance every new attempt. What I learned from every attemp was that the number of hidden layers and the number of neurons had an impact on increasing the model accuracy. 
   


