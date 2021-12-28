# MLandWeatherProject
Project to explore Machine Learning and Weather Prediction
The goal is to see how well we can predict the Average Daily temperature on a day using the three previous days weather data using machine learning models.

I. Gathering the Weather Data
Intial gathering and cleaning of the data from personal weather stations using weatherunderground API. Difficulty was/is finding a weatherstation with a nearly complete data set over the range of dates you are looking to gather data from. From there the data is placed in a Pandas Dataframe and you clean the data of the null values(there will probably always be some). Next create an offset columns for three days prior data(e.g. for TempAvg create TempAvg_1, TempAvg_2, TempAvg_3) for each variable to be used in the model training. Then simply pickle the file for the next step.

II. Applying Linear Regression to Predict Weather
Unpickle the Pandas dataframe from the last step, and perform some statistical analysis to determine what variables correlate best to the TempAvg we are attempting to predict. From there wittle down the number of variables to only a few that are the most useful. Then using these variables and SciKit-learn create a basic linear-regression model using the variables you decided upon in the last step, and analyze how well the model fits the data.

III. Using Neural Networks to Predict Weather
Finally unpickle the original Pandas dataframe yet again, and this time split the data using Scikit-learns training_test_split into your training and testing data sets. From here set up your TensorFlow Neural Network Regressor Model to be trained, and allow it to run(usually takes a good while). Then analyze how well the model was trained to fit the data, by graphing the loss function compared to the number of steps taken. This will allow you to see whether or not you've run into the problem of overtraining. Lastly, analyze how well the model fits the data just as you did in the Linear Regression portion. With this you can now compare how  well the DNNRegressor model performs compared to the standard linear regression model. 

This project was based on [this stack abuse article](https://stackabuse.com/using-machine-learning-to-predict-the-weather-part-1/) by Adam McQuistan. 
