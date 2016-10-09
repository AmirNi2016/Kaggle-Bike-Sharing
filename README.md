# Kaggle-Bike-Sharing
This is an ongoing project on [Kaggle's Bike Sharing problem](https://www.kaggle.com/c/bike-sharing-demand). I explopre the data, preprocess, visualize, analyze and an try different linear and nonlinear regression models and compare their performance on the data set. Each section is treated in a separate ipython notebook for ease of review.

### 01 - [Kaggle - bike share system -  Problem formulation](https://github.com/AmirNi2016/Kaggle-Bike-Sharing/blob/master/01%20-%20Kaggle%20-%20bike%20share%20system%20-%20problem%20formulation.ipynb)
Description of the problem, the data set (features, targets) and discussion of the evaluation metric.

### 02 - Kaggle - bike share system - Data preprocessing
Preprocessing: using pandas' time series capabilities, we extract numerical values of date (year, month, day) and time (hour) from the `datetime` column. Also, we make one additional data set where the categorical data are represented by dummy matrices.

### 03 - Kaggle - bike share system - data visualization
Exporatory data analysis: we plot the average number of customers for different day time periods, weekdays and months over the two year time span. We use groupby and aggregate capabilities of the panadas to obtain the average number of customers for different scenarios (see **Tutorial - Multi Indexig and Groupby in Pandas.ipynb** for a tutorial on code details).
The plots show that the business had had growth from 2011 to 2012. Casual customers use the system more on weekends while registerd customers use the system more on workdays. The data shows a seasonality pattern. The maximum usage is between 10:00 am and 5:00 pm. 

### 04 - Kaggle - bike share system - Adding customer average to the features
We would like to extract the maximum possible information from the data to train our model. Since Kaggle's bike sharing challenge is an intrapolation problem (except for December 2012 with is an extrapolation), it is reasonable hypothesis to assume that the unknown customer number during the last ten days of each month is close to the average of the known values for each weekday and time frame. So, in our first attempt, we add these average values as new columns of features. FOr this purpose we use pandas' groupby, aggregation, and multi-indexing capabilities. The new data frames are stored as new CSV files.








