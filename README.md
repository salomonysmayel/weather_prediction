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

![supply_chain](/images/neural_net_res1.png)

![supply_chain](/images/neural_net_res2.png)

![supply_chain](/images/ml_model_results.png)

![supply_chain](/images/ml_model_results2.png)

![supply_chain](/images/pca.png)

![supply_chain](/images/pca2.png)

![supply_chain](/images/pca_results1.png)

![supply_chain](/images/pca_results2.png)

![supply_chain](/images/arima_noise.png)

![supply_chain](/images/arima_trend.png)

![supply_chain](/images/arima1.png)

![supply_chain](/images/arima2.png)

![supply_chain](/images/arima3.png)



