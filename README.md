# Predicting Movie Box Office Revenue Project

<h2>Overview</h2>
    The goal of this project was to use linear and polynomial regression models to predict box office revenue generated by different movies. This project idea was     sourced from kaggle.com and the movie data set if from The Movie Database. The train.csv file from kaggle.com was downloaded and used throughout this project as it contained movie feature data along with true box office revenue for each movie observation. The 3,000 movie observations were split into training and test data, and the performance metrics for various linear and polynomial regression models were calculated to determine the best regression model to predict movie box office revenue.

<h2>Processing Data & Creating a Correlation Matrix:</h2>
To begin this project, a few of the features in the movie data set needed to be processed into data usable for linear and polynomial regression analyses. Specifically, three of the movie data features, to include the belongs to collection, original language, and release date features, needed to be represented in a numerical way so they could be incorporated into the different regression analyses. The belongs to collection movie data feature indicates whether or not a movie is part of a series of related movies; the belongs to collection feature was processed to numerical data feature by assigning an integer label of 0 to movies that are not part of a collection and a label of 1 to movies which are part of a collection. Next, the original language movie data feature was processed to a numerical feature. The original language movie data feature expresses the original language that the movie was filmed in, for example, a movie observation might have an original language value of “en” indicating that the movie was filmed in English. Numerical integer labels ranging from 1 through 6 were used to numerically label the original language movie data feature. The final movie data feature which needed to be processed into a numerical data set was the release date feature. The release date values for each movie observation were represented in MM/DD/YYYY format; the integer number of the month the movie was released was parsed from the data and used to provide a numerical representation of the release date feature. The newly derived numerical data features were added as columns of data to the rest of the movie data to support the regression analyses performed in this project.


