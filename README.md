<h2> Greater Toronto Area Property Prices Regression</h2>
<h4> Project Description </h4>
<p> 
This project aims at predicting prices of houses in the greater Toronto area based on a dataset from <a href='https://www.kaggle.com/datasets/mangaljitsingh/torontoproperties/code'>Kaggle</a>.<br>
</p>
<h4> Step-by-Step Solution </h4>
<p>
The following steps are used to predict the prices:<br>
<ol>
<li> <strong> Explanatory Data Analysis: </strong> In order to better understand different features, the relationship with each other, and their impact on the output, explanatory data analysis is conducted </li>
<li> <strong> Data Preprocessing: </strong> To process the data with machine learning regression models the categorical data has to be transformed into numerical data and scaled to better balance the impact of different features </li>
<li> <strong> Model Selection and Training: </strong> The best model is selected based on root mean squared error= and trained on the data for the regression </li>
</ol>
</p>
<h4> Explanatory Data Analysis</h4>
<p>
First of all, the distribution of the price is investigated as it can be seen in the following image.<br>
<br>
<img src='https://github.com/AliAbbasiSh/Property-Price-Regression/blob/main/Price%20distribution.png'><br>
<br>
following that, average price based on different factors such as number of bedrooms and region are illustrated and finally the correlation between different parameters are shown as a heatmap.<br>
<br>
<img src='https://github.com/AliAbbasiSh/Property-Price-Regression/blob/main/Price%20correlation.png'><br>
<br>
The effect of the number of bathrooms and bedrooms are evident in this heatmap
</p>
<h4> Data Preprocessing </h4>
<p>
in this step, the region columns is transformed using one hot encoding and the resulting data are scaled using min-max scaling method.<br>
</p>
<h4> Model Selection and Training </h4>
<p>
in this step, first some of the basic models such as linear and ridge regression are trained. As evident in the next graph these methods have limited success and the RMSE is approximately 1.05M dollars<br>
<br>
<img src='https://github.com/AliAbbasiSh/Property-Price-Regression/blob/main/Linear%20Regression.png'><br>
<br>
The next step is to use some of the more sophisticated models such as random forest and XGboost which significantly improve the result. Using gridsearch we are able to imporve the result further and achieve a RMSE of 985k dollars.
<br>
<img src='https://github.com/AliAbbasiSh/Property-Price-Regression/blob/main/Random%20Forest%20Regression.png'><br>
<br>
However, the best result is achieved by using a deep learning model of 4 hidden layers of 33 units. The RMSE using this method is 961k dollars.
<br>
<img src='https://github.com/AliAbbasiSh/Property-Price-Regression/blob/main/Neural%20Network%20Regression.png'><br>
<br>
</p>
