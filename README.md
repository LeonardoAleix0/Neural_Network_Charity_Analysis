# Neural_Network_Charity_Analysis


## Overview of Project


This project’s objective is to create a deep-learning neural network to analyze and classify the success of charitable donations. 
The deliverables for this project are:

*	Preprocess data for a Neural Network model.

* Compile, Train and Evaluate the model.				

*	Optimize the model to achieve a target predictive accuracy higher than 75%.

## Software


Python, Pandas Jupyter notebook and TensorFlow. 

## Results 


### Preprocess data for a Neural Network model.


In this stage of the data manipulation, the variables that are considered target and feature were identified. Columns EIN and NAME were removed, a density plot was created to determine binning.
Using One-hot encoding, the categorical variables were encoded and placed in a new dataframe. The one-hot encoding dataframe was merged to the original dataframe and the original values were dropped.


![image](https://user-images.githubusercontent.com/86136535/140661340-462466f8-16cb-4743-ba93-4fdd4b3039d6.png)

 
### Compile, Train and Evaluate the model.


A neural network was created with two hidden layers using TensorFlow.


![image](https://user-images.githubusercontent.com/86136535/140661356-51403505-2b61-482a-a367-66522d077563.png)
 

The model was compiled and trained with 100 epochs; the accuracy test result was 72%.


![image](https://user-images.githubusercontent.com/86136535/140661366-2ef69a90-6802-4596-a748-03684229acaf.png)



### Optimize the model to achieve a target predictive accuracy higher than 75%.

Attempt 1 - I decided to add a third hidden layer with 30 nodes maintaining the same number of epochs, there were no significant changes in the accuracy result (72%).


![image](https://user-images.githubusercontent.com/86136535/140661373-fe8ffb13-0037-4b34-b92c-69a66636c340.png)



Attempt 2 – On my second attempt, I kept the same set up as the attempt 1 but decided to do a binning on the column INCOME_AMOUNT based on the results of a density plot. 


![image](https://user-images.githubusercontent.com/86136535/140661385-9847c1c4-8016-47eb-b781-214cb1290036.png)

 
The results were not significant, the accuracy continues on 72%.


![image](https://user-images.githubusercontent.com/86136535/140661394-43716a96-e47d-4e78-ba5f-e730eef64539.png)


Attempt 3 – I kept the same set up as the attempt 1 but decided to do a binning on the column INCOME_AMOUNT and NAME, the accuracy increased in 1% (73%).


![image](https://user-images.githubusercontent.com/86136535/140661400-95a09e2d-f31a-4282-9a51-5c0c07180168.png)



Attempt 4 – Kept three hidden layers, kept columns NAME and INCOME_AMOUNT, epochs = 100 and added a dropout layer between layer two and three. There was a significant increase in the accuracy results 78%.
 

 ![image](https://user-images.githubusercontent.com/86136535/140661415-827b6d08-76bc-452e-901a-b03e43d9cbd3.png)
 
 
 ![image](https://user-images.githubusercontent.com/86136535/140661418-7365cd5e-1f67-4662-bf32-16ed94c8427c.png)



### Summary.


Not all the attempts to increase the accuracy of this model were included in this project. Within these attempts, data manipulation, increase and decrease of hidden layers were attempted however it did not translate to any significant change. 
The introduction of dropout layer changed the outcome of the results, increasing the accuracy from 72% to 78%. This significant change is due to the fact that dropping 25% of neurons, increased the randomness of the model which resulted in a better pattern reading increasing the accuracy result.
