# Neural_Network_Charity_Analysis
Preprocessing Data for a Neural Network Model, compile, traing and evaluate the model then optimize it. 

## Overview

The purpose of this project is to analyze 34,000 organizations that have received funding from Alphabet Soup using neural networks and create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. The study will consist of 3 technical analysis :
- Preprocessing Data for a Neural Network Model
- Compile, Train, and Evaluate the Model
- Optimize the Model


## Results 

### Data Processing
We first examine the data to identify the variables that are considered to be the target, features or are neither targets nor features, and should be removed from the input data for our model.
The charity dataset contains information on EIN(Enployee Identifier), NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT,SPECIAL_CONSIDERATIONS, STATUS, and ASK_AMT.
- The variable(s) that are considered as to be target for our model is "IS-SUCCESSFUL" coulumn. It's the most important variable in the dataset as it determines the effectiveness of the fundings. 
- The variable(s) cthat are considered as to be features for our model are APPLICATION, TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT,SPECIAL_CONSIDERATIONS, STATUS, and ASK_AMT.
- The variable(s) are neither targets nor features, and should be removed from the input data are the "EIN", "AFFILIATION","STATUS" columns as they are not relevant for our model and can create confusion.   
 
 ![name](https://github.com/assaci/Neural_Network_Charity_Analysis/blob/main/name.PNG?raw=true)
  
 ![app_type](https://github.com/assaci/Neural_Network_Charity_Analysis/blob/main/app_type.PNG?raw=true)
  
 ![class](https://github.com/assaci/Neural_Network_Charity_Analysis/blob/main/class.PNG?raw=true)
 
 ![preprocessed](https://github.com/assaci/Neural_Network_Charity_Analysis/blob/main/preprocessed.PNG?raw=true)

### Compile, Train, and Evaluate the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
There are 2 hidden layers in our model. The first hidden layer has 100 neurons and the second has 50 neurons. The activation function used for both layers is "relu" and the output layer activation function is "sigmoid".
I selected these layers because they seem to increase the accuracy.

- Were you able to achieve the target model performance?
Yes, I was able to to achieve the target model performance. 

- What steps did you take to try and increase model performance?
I first dropped columns "EIN" and "NAME" then set 4 different hidden layers to 80, 30, 20, and 10  neurons but I noticed  I was getting less than 53% accuracy.
To increase the model performance, I added back the column "NAME" then removed "EIN", "AFFILIATION", "STATUS" columns. I decrease the number of hidden layers and increase the neurons. I was able to increase the accuracy from 53% to 76%. 

 ![layers](https://github.com/assaci/Neural_Network_Charity_Analysis/blob/main/layers.PNG?raw=true)
 
  ![Accuracy](https://github.com/assaci/Neural_Network_Charity_Analysis/blob/main/Accuracy.PNG?raw=true)

## Summary 

Our model ended up reaching 76% accuracy. The focus o the study was to predict whether applicants will be successful if funded by Alphabet SoupBased. We had a dataset that contained information from 34,000 organizations that have received funding from Alphabet Soup. We examined the dataset, narrowed down the columns for cleaning selected the target and features that were relevant for our model. Base on our analysis, we determined that 3 futeares were significant for the prediction: Name, Application_type, and Classification. In conclusion, any applicant who has the following characteristics will have a 76% of chance of being successful with Alphabet Soup fundings:
- Their NAME appears more than 5 times.
- Their APPLICATION_type is one of the following; T3, T4, T5, T6, T7, T8, T10, and T19
- The application has the following CLASSIFICATION; C1000, C2000, C3000, C1200, and C2100.

Even if we reached more than 75% accuracy, we could get a much higher accuracy rate by having more data for our model.  

