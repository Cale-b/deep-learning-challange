# deep-learning-challange

The purpose of this analysis is to use our new skills of deep learning to optimize a given dataset

## Data Background
The data we are using for this project is from a non-profit organization called Alphabet Soup. The dataset 
has information from 34,000 applications by different companies for funds. The metadata included is the 
name, application type, afflitation, classification, status, income_amt of each company that has 
applied for funding.

## Analysis
### DATA PRE-PROCESSING
The data processing for this project included determining the X and Y targets for the model being created. These
targets were determined to be based on if the application was successful, and if the application was not successful.
After determining the targets we needed to narrow down the variables of the data to make the model more accurate.
These variables included Application_type and Classification. These variables were narrowed down to application_type T3 
or Other and Classifcations C1000,C1200,C2000 and Other. WE removed all the variables that did not fall within the range 
we had selected for Application_type and Classification.

### COMPILING, TRAINING, AND EVALUATING THE MODEL
After doing all the data pre-processing it is time to compile, train and evaluate the model.
#### COMPILE
Before we can complile the model we first had to define the model. THe model that was chosen was the Keras Sequential Model. 
Following the selection of the model we needed to create the first and second hidden layer and the output layer. These layers
are where we get to decide the # of nuerons, and activation function for the model. For the first model it was decided to use 
80 nuerons in the first hidden layer with the activation of RELU, 30 nuerons in the second hidden layer also with RELU activation, 
and finally in the output layer to use the activation of Sigmoid. 
#### TRAINING
After determining the nuerons, layers, and activation functions for the model we then have to train it with the test data. The training
includes picking a number of epochs, or # of times to test the data, which was picked to be 100. The model was then ran to fit the test 
data and the accuracy, lose, and recall was then calcauted for each epoch.
#### EVALUATION
The accuracy, lose and recall of the trained model was then ploted to evalaute the results. THe results shoew that the model had an accuracy 
of 76%.

![Screenshot 2023-05-24 210652](https://github.com/Cale-b/deep-learning-challange/assets/93220886/d7bd3ffb-11be-4ca8-94e0-0ef05cd4a521)

### OPTIMIZATION

#### OPTIMIZATION 1
TO better optimize this model I doubled the amount of neurons(160 & 60). That resulted in a slightly lower accuracy of 75.6%, but the 
chart is much more linear showing that increasing the neurons seems to have an impact on the lose calculated.


![Screenshot 2023-05-24 210707](https://github.com/Cale-b/deep-learning-challange/assets/93220886/e9f3cef7-702c-45d7-a5f5-55b7b6dc13d4)

#### OPTIMIZATION 2
For this optimization i doubled the alreadt doubled amounts of neurons(320 & 120). Doing this seemed to decrease the accuracy to 73%. While
also making the chart look similar to the original model
![Screenshot 2023-05-24 220337](https://github.com/Cale-b/deep-learning-challange/assets/93220886/3315bdb3-4615-4b91-b516-919a75a3a373)

## CONCLUSION
Looking at the charts and accuracy I would recommend that the company start with my first optimization and optimize it further if they wanted better
resutls.

If i wanted to change the model I'd add more hidden layers, maybe change the activation and also make the loss part of compliing multiple instead of
binary. These changes could have major changes to my results.
