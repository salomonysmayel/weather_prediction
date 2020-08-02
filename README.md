# Temperature Forecasting with Machine Learning

Climate is the average state of the atmosphere over long periods of time. Weather refers to day to day temperature and precipitation activity. Most weather phenomena occurs in the lowest levels of the atmosphere. These states are described by meteorological variables such as wind speed, atmospheric pressure and temperature. 
Each one of these variables can be presented as a time series, were there is noise but also clear patterns, moreover, some of these variables are highly correlated. This presents a great opportunity to perform Machine Learning to forecast the variables. In this case Temperature. 

## The Data 

The dataset used on this project is a weather time series recorded at the Weather Station at the Max Planck Institute for Biogeochemistry in Jena, Germany. In the dataset 14 different variables were recorded every 10 minutes. The data used is from 2009 to 2016. Some of the variables are: temperature, atmospheric pressure, humidity and wind direction.

![supply_chain](/images/data.png)

### Density distributions of each data variable

![supply_chain](/images/d_1.png)

![supply_chain](/images/d_2.png)

![supply_chain](/images/d_3.png)

### Temperature Time Series

![supply_chain](/images/temp.png)

The variables are correlated as follows

![supply_chain](/images/corr.png)

The following heatmap presents the correlation between the variables in a more graphic manner, were the lighter the color the higher the correlation and viseversa

![supply_chain](/images/heat.png)

Now we proceed to normalize the data so that the ranges of values of the variables are not so disimilar.

![supply_chain](/images/normalization.png)

The first machine learning model to build is a gradient boosting

![supply_chain](/images/gradient_boosting.png)

the second machine learning model to build is a XG-Boost

![supply_chain](/images/xg_boost.png)

![supply_chain](/images/xg_boost_feature_importance.png)

Finally a Neural Network is build

![supply_chain](/images/neural_net.png)

The following to graphs present the validation errors of the trainning proccess for the Neural Network. On the model loss vs epochs we can see how both train and validation go down and converge, which indicates that the model was not overfitted nor underfitted, which is the desirable outcome. 

![supply_chain](/images/neural_net_res1.png)

![supply_chain](/images/neural_net_res2.png)

The following chart shows the result for the three machine learning models, to predict temperature. The second column is the real values from the test set, and the folllowing columns are the predicted values. 

![supply_chain](/images/ml_model_results.png)

The mean suarqed errors of these predicted values with the real values are shown bellow.

![supply_chain](/images/ml_model_results2.png)

Then a Principal Component Analysis was performed on the data to see if we could improve the results. In this case to go from 13 features to 6.

![supply_chain](/images/pca.png)

![supply_chain](/images/pca2.png)

With this new reduced dataset the ML models were trainend again, the results below.

![supply_chain](/images/pca_results1.png)

![supply_chain](/images/pca_results2.png)

Comparing the mean square erros with the results from the data without PCA shows that in this case PCA did not help to improve the results.

Finally a time series analysis was performed, just with the temperature, to try to predict temperature values five steps ahead into the future.

![supply_chain](/images/arima_noise.png)

![supply_chain](/images/arima_trend.png)

![supply_chain](/images/arima1.png)

![supply_chain](/images/arima2.png)

Predictions 50 minutes into the future with time series analysis.

![supply_chain](/images/arima3.png)



