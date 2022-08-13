# Predicting Movie Box Office Revenue Project

<h2>Overview</h2>
<p>The goal of this project was to use linear and polynomial regression models to predict box office revenue generated by different movies. This project idea was     sourced from kaggle.com and the movie data set if from The Movie Database. The train.csv file from kaggle.com was downloaded and used throughout this project as it contained movie feature data along with true box office revenue for each movie observation. The 3,000 movie observations were split into training and test data, and the performance metrics for various linear and polynomial regression models were calculated to determine the best regression model to predict movie box office revenue.</p>

<h2>Processing Data & Creating a Correlation Matrix:</h2>
<p>To begin this project, a few of the features in the movie data set needed to be processed into data usable for linear and polynomial regression analyses. Specifically, three of the movie data features, to include the belongs to collection, original language, and release date features, needed to be represented in a numerical way so they could be incorporated into the different regression analyses. The belongs to collection movie data feature indicates whether or not a movie is part of a series of related movies; the belongs to collection feature was processed to numerical data feature by assigning an integer label of 0 to movies that are not part of a collection and a label of 1 to movies which are part of a collection. Next, the original language movie data feature was processed to a numerical feature. The original language movie data feature expresses the original language that the movie was filmed in, for example, a movie observation might have an original language value of “en” indicating that the movie was filmed in English. Numerical integer labels ranging from 1 through 6 were used to numerically label the original language movie data feature. The final movie data feature which needed to be processed into a numerical data set was the release date feature. The release date values for each movie observation were represented in MM/DD/YYYY format; the integer number of the month the movie was released was parsed from the data and used to provide a numerical representation of the release date feature. The newly derived numerical data features were added as columns of data to the rest of the movie data to support the regression analyses performed in this project.</p>

<p>A correlation matrix was created to see which movie data features correlated closely with the box office revenue. The movie budget feature had the highest correlation value of 0.75 and the movie popularity had the second highest correlation value of 0.46. The movie feature correlation matrix is shown in the Appendix: Movie Feature Correlation Matrix.</p>

<h2>Linear Regression Analysis:</h2>
<p>Various linear regression analyses were performed to predict the box office revenues for movie observations. First, a linear regression model with a single feature, the movie popularity feature, was used to predict the box office revenue for the movie observations in the test data set. The movie popularity feature was chosen as it was fairly well correlated with the movie box office revenue; the correlation between the movie popularity and box office revenue was 0.46. The single feature linear regression model with movie popularity as the feature resulted in a low coefficient of determination (R2) value of 0.18 and a high root mean square error (RMSE) of 1.22E8. A plot of the Movie Popularity vs. Movie Revenue with a line of best fit, the predicted values, can be found in the Appendix: Single Feature Linear Regression Plot. Next, a linear regression analysis was performed with all the movie data features; this yielded a fairly good R2 value of 0.65 and a much lower RMSE of 8.35E7. Finally, a linear regression analysis using the K-best features method was used with k-feature values ranging from 1 through 5; a K-best of six features was not used as 6 features were used in this analysis and an analysis will all the features was previously performed. The K-best linear regression model with 3 features, which included the movie budget, movie popularity, and collection label features, yielded the best results. The K-best model with k=3 resulted in an R2 value of about 0.64 and a RMSE of 8.36E7. The performance metrics for all the linear regression models used in this analysis can be found in the Appendix: Linear Regression Model Performance Table. Overall, the K-best linear regression model with k=3 features resulted in the most accurate movie box office revenue predictions; the Mean Absolute Error (MAE) of the revenue predictions for this model was $45,120,081.42.</p>

<h2>Polynomial Regression Analysis:</h2>
<p>Next, several different polynomial regression analyses were performed to predict the box office revenues for movie observations. First, a single feature polynomial regression analysis was complete with n-degree values ranging from 2 through 6. The single feature that was chosen to train these polynomial models with was the movie budget data feature as it was the single best predictor variable based on the K-best linear regression analysis. The performance metrics were computed and a plot of the Movie Budget vs. Movie Revenue wit a line of best fit, the predicted values, was created for each n-polynomial regression model. The Movie Budget vs. Movie Revenue plot for the single feature polynomial regression model with n-degree=3 can be found in the Appendix: Single Feature Polynomial Regression Plot. The best performing single feature polynomial regression model was with n-degree=3; this model yielded an R2 value of 0.57 and a RMSE of 8.89E7. Next, a multiple feature polynomial regression analysis was performed with all the movie data features. Utilizing all of the movie data features improved the accuracy of the predictions; the best multiple feature polynomial regression model was with n-degree=2. The n-degree=2 multiple feature polynomial model resulted in an R2 value of 0.67 and a RMSE of 8.01E7. The performance metrics for all the polynomial models used in this analysis can be found in the Appendix: Polynomial Regression Model Performance Table. Overall, the best polynomial regression model was the multiple feature polynomial regression model with n-degree=2 as this model yielded the highest R2 value and lowest RMSE; the MAE of the revenue predictions for this model was $ 41,502,645.73.</p>

<h2>Conclusion:</h2>
<p>From this regression analysis project, it is evident that both linear and polynomial regression models can be used to predict movie box office revenue with some degree of accuracy. The multiple feature linear regression models performed surprisingly well, but the multiple feature polynomial regression models yielded the best results. Out of all of these models, the multiple feature polynomial regression model with n-degree=2 provided the most accurate movie box office revenue predictions and would be the model of choice for this problem. Lastly, the steps to run the source code can be found in the Appendix:</p>

<h2>Appendix:</h2>
<h3>Movie Feature Correlation Matrix</h3>
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)

<h3>Single Feature Linear Regression Plot</h3>

<h3>Linear Regression Model Performance Table</h3>

<h3>Single Feature Polynomial Regression Plot</h3>

<h3>Polynomial Regression Model Performance Table</h3>
