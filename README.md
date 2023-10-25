# Deep-Learning-Challenge

## The Neural Network Model Analysis

## Overview and Results
Creating a deep learning model for a nonprofit called Alphabet Soup, a dataset of applicant information was used to predict if funding from Alphabet Soup would be successful for their ventures. Multiple models of machine learning and neural networks were used to try to reach at least 75% accuracy. The data was processed then the initial model was compliled, trained and evaluated for accuracy. After reaching only 72.65% on the first attempt, the model was optimized three addtional times to attempt to increase the accuracy. 


<img width="584" alt="Screenshot 2023-10-25 at 11 30 56 AM" src="https://github.com/marlablanco/Deep-Learning-Challenge/assets/131930449/de5cef54-b482-4d40-a1d2-cc1a28754eff">

<img width="618" alt="Screenshot 2023-10-25 at 11 31 09 AM" src="https://github.com/marlablanco/Deep-Learning-Challenge/assets/131930449/f6292005-928e-48b7-8132-52f3456fdd6e">



The second model included an additional hidden layer (values of 80, 40, and 20) and increased epochs from 50 to 75. This increased the accuracy of the model very slightly to 72.79%.

<img width="578" alt="Screenshot 2023-10-25 at 11 34 11 AM" src="https://github.com/marlablanco/Deep-Learning-Challenge/assets/131930449/67e9cc2a-7b08-43a4-ac98-33b868b297d2">

<img width="621" alt="Screenshot 2023-10-25 at 11 34 21 AM" src="https://github.com/marlablanco/Deep-Learning-Challenge/assets/131930449/c94b0a96-6343-4dd6-8f2c-6fde6ecaf28e">



The third model added one more hidden layer (values of 90, 30, 30) and increased the epochs to 100, resulting in an accuracy of 72.98%.


<img width="582" alt="Screenshot 2023-10-25 at 11 35 03 AM" src="https://github.com/marlablanco/Deep-Learning-Challenge/assets/131930449/2982580e-0f71-4cc8-8d73-b19ee9606380">

<img width="614" alt="Screenshot 2023-10-25 at 11 35 13 AM" src="https://github.com/marlablanco/Deep-Learning-Challenge/assets/131930449/ca212b2c-19c3-482a-b3ab-6f57d23d6c93">




The fourth and final model added back the NAME column and binned it with the APPLICATION_TYPE and CLASSIFICATION. In addition to maintaining three hidden layers (values of 100, 50, 25) and epochs set to 50, the addition of the NAME column brought the accuracy percentage up to 74.09%, almost to the goal of 75%.


<img width="585" alt="Screenshot 2023-10-25 at 11 35 52 AM" src="https://github.com/marlablanco/Deep-Learning-Challenge/assets/131930449/bc7f03bf-e8ca-4854-b601-68a57a8a8daa">
<img width="634" alt="Screenshot 2023-10-25 at 12 27 17 PM" src="https://github.com/marlablanco/Deep-Learning-Challenge/assets/131930449/2827d894-1627-4bf7-8256-f97c95a15325">



Typically, increasing the number of hidden layers and epochs can help the model's accuracy, the decrease in accuracy on the first and second optimization models can be due to a number of reasons including overfitting the model, increasing training time or computational inefficiencies because of its complexity.

## Data Processing
### - What variable(s) are the target(s) for your model?
- The target variable was "IS_SUCCESSFUL." 1 being yes and 0 being no.
### - What variable(s) are the features for your model?
- The feature variables included:
APPLICATION_TYPE,
AFFILIATION,
CLASSIFICATION,
USE_CASE,
ORGANIZATION,
STATUS,
INCOME_AMT,
SPECIAL_CONSIDERATIONS, and 
ASK_AMT
### - What variable(s) should be removed from the input data because they are neither targets nor features?
- EIN and NAME were removed from the input data because they are not considered target or feature variables. The NAME column was added back in for the fourth model and brought the model's accuracy percentage up slightly.
  
## Compiling, Training, and Evaluating the Model
### - How many neurons, layers, and activation functions did you select for your neural network model, and why?
- 1st model: 2 hidden layers with 80, 40 neurons split. The hidden layer activation function used was relu.
Output node is 1 because it was a binary classifier model using the sigmoid function as the output activation. 
- 2nd model: Increased to 3 hidden layers with 80, 40, 20 neurons split. The hidden layer activation functions were still relu and the sigmoid function was also still used for the output.
- 3rd model: Stayed with 3 hidden layers with 90, 30, 30 neurons split. The hidden layer activation functions, again, were relu with the sigmoid function for output activation.
- 4th model: Stayed with 3 hidden layerswith 100, 50, 25 neurons split. The hidden layer activation functions, again, were relu with the sigmoid function for output activation.
### - Were you able to achieve the target model performance?
- With the first three iterations of the models, I was unable to achieve the target 75% accuracy. However, after adding back and binning the NAME column, the accuracy of the model got to 74%, which was the closest attempt. 
### - What steps did you take in your attempts to increase model performance?
- With each new model, I either changed the number of hidden layers or value of neurons, and increaed the epochs each time with the intention of increasing model performance. In this case, these steps actually decreased accuracy output. The final and most successful model included 3 hidden layers but kept the epochs at 50 to try to reduce overfitting. By binning and not removing the NAME column, the final model was able to almost successfully achieve the requested accuracy, off by just 1%.

## Summary
After multiple attempts at creating a neural network model that performs at a minimum of 75% accuracy for the Alphabet Soup Foundation, I was able to nearly successfully obtain desired accuracy by increasing hidden layers, changing the hidden node values, and increasing or decreasing epochs. Not removing then binning the NAME column to keep as a feature made the greatest diffrence in the end and brought the accuracy to 74%.
