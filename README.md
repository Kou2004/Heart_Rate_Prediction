# Heart_Rate_Prediction
This project has been made during the AI-Parsec Hackathon conducted by IIT dharwad. Use a voting Regressor to solve this problem get upto 99% accuracy. Acheieved 27th Rank in this hackathon.

# Is it a time series data?
According to me, its no, because
- No timeStamp column is given to us, which creates a problem in the prediction of the time series data, as here we need to have equal timestamp data to make accurate predictions.
- Also the target column is very much stationary, you can see from the plot given in the notebook. Very less variance are there, with a constant mean.
- Also , this data is given for different patients, not for single patient. Clearly it is a regression problem
  
# Why Voting Regressor & what are the alternatives for that model ?
- I have tried with linear regression first, but it has been clearly seen that features are not such a linearly related to the target, which can affect the model performance, also many features are correlated.
- When I use different types of the boosting algorithms, I have found every algo is able to capture non-linearities of the data very well resulting in the high accuracy. We all know voting / ensemble method uses the hard voting mechanism , which results in the more higher and strong robust model than the others, also seen from the results.
- If I talk about the alternative , I guess Polynomial Linear Regression can perform well on the problem, but due to lack of time , I am unable to apply it on the P.S. But I have choose the Boosting algorihtms , as the many features are highly correlated with each other resulting in the wrong determination of the regression coefficients.

# Improvemnents 
- I guess more hyperparameter tuning with the gridSearch can results in the better results.
- We can use SMOTE to generate data for the outliers points (HR >= 100) ,and then train it again , to capture more non-linearities of the data, such that model perfoms well on the outliers also.
