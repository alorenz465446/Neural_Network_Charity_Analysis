# Neural_Network_Charity_Analysis
 
 ## Overview

Creating a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special consideration for application
* ASK_AMT—Funding amount requested
* IS_SUCCESSFUL—Was the money used effectively
 
 These are the steps I will follow:
 
* Preprocessing Data for a Neural Network Model
* Compile, Train, and Evaluate the Model
* Optimize the Model
 
 
 ## Results
 
### Data Preprocessing

* The "Is-Successful" column was the target for this model. It defines whether or not the money was used practically.

* NAME, APPLICATION, TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT,SPECIAL_CONSIDERATIONS, STATUS, and ASK_AMT were the features of this model.

* EIN (Employer identificaiton) was dropped because the numbers could confuse the system into thinking its significant. ANSWER: A student could drop SPECIAL_CONSIDERATIONS because there is only a small percentage of cases that had any special consideration, and special considerations cannot be quantified. 

* A student could drop STATUS because all rows were the same value, 1.

### Compiling, Training, and Evaluating the Model

* There are three hidden layers in this model, each with many neurons. These hidden layers seeemed to increase the accuracy above 75%. The number of epochs was not morphed. First activation function was 'relu'. Second and third were 'sigmoid' (helped boost accuracy). The output function was 'sigmoid'. 

* I was able to achieve the target model performance.

* Converting the NAME column into data points was needed because it had the most impact on improving efficiency. A third layer and using the "sigmoid" activation function for the 2nd and 3rd layer was also used.
 
 ## Summary

We can accurately classify each of the test data points 75% of the time by raising the accuracy over 75%. Additionally, if an applicant possesses the following, they have an 80% chance of being accepted:

* NAME appears more than 5 times (applied > 5 times)
* APPLICATION is one of these; T3, T4, T5, T6, T7, T8, T10, and T19
* CLASSIFICATION; C1000, C2000, C3000, C1200, and C2100 is listed 

A reccomendation is the Random Forest model. This model would be good because it is works well with classification problems.
