# Problem Statement
A Chinese automobile company Geely Auto aspires to enter the US market by setting up their manufacturing unit there and producing cars locally to give competition to their US and European counterparts.

They have contracted an automobile consulting company to understand the factors on which the pricing of cars depends. Specifically, they want to understand the factors affecting the pricing of cars in the American market, since those may be very different from the Chinese market. The company wants to know:

* Which variables are significant in predicting the price of a car
* How well those variables describe the price of a car

# Dataset
The dataset used is the [CarPrice Prediction MLR+RFE+VIF](https://www.kaggle.com/hellbuoy/carprice-prediction-mlr-rfe-vif/notebook#Step-6:-Building-a-Linear-Model) from Kaggle. 

**The 26 variables are:**

1.car_ID              205 non-null int64

2.symboling           205 non-null int64

3.CarName             205 non-null object

4.fueltype            205 non-null object

5.aspiration          205 non-null object

6.doornumber          205 non-null object

7.carbody             205 non-null object

8.drivewheel          205 non-null object

9.enginelocation      205 non-null object

10.wheelbase           205 non-null float64

11.carlength           205 non-null float64

12.carwidth            205 non-null float64

13.carheight           205 non-null float64

14.curbweight          205 non-null int64

15.enginetype          205 non-null object

16.cylindernumber      205 non-null object

17.enginesize          205 non-null int64

18.fuelsystem          205 non-null object

19.boreratio           205 non-null float64

20.stroke              205 non-null float64

21.compressionratio    205 non-null float64

22.horsepower          205 non-null int64

23.peakrpm             205 non-null int64

24.citympg             205 non-null int64

25.highwaympg          205 non-null int64

26.price               205 non-null float64


**Target Variable:**

Price (float64)

**Price** refer to the car price based on the 26 variable covering most combination for a particular type.We are required to model the price of cars with the available independent variables. It will be used by the management to understand how exactly the prices vary with the independent variables. They can accordingly manipulate the design of the cars, the business strategy etc. to meet certain price levels. Further, the model will be a good way for management to understand the pricing dynamics of a new market.

# Data Cleaning Methodology 

**Rescaling the Features**

For Simple Linear Regression, scaling doesn't impact model. So it is extremely important to rescale the variables so that they have a comparable scale. If we don't have comparable scales, then some of the coefficients as obtained by fitting the regression model might be very large or very small as compared to the other coefficients. There are two common ways of rescaling:

1. Min-Max scaling

3. Standardisation (mean-0, sigma-1)

Here, we will use Standardisation Scaling.

**Recursive Feature Elimination, or RFE**

It is a popular feature selection algorithm.

RFE is popular because it is easy to configure and use and because it is effective at selecting those features (columns) in a training dataset that are more or most relevant in predicting the target variable.
[Refer](https://machinelearningmastery.com/rfe-feature-selection-in-python/)

**Variance Inflation Factor or VIF**

It gives a basic quantitative idea about how much the feature variables are correlated with each other. It is an extremely important parameter to test our linear model. The formula for calculating VIF is:

**VIFi=1/(1-Ri^2)**
[About VIF and how multicollinearity effects Regression and requires VIF calculation](https://www.google.com/url?q=https://www.statology.org/multicollinearity-regression/&sa=D&source=editors&ust=1642878176744517&usg=AOvVaw14ZRypqIN5j8F9g_0L5ZXC)

# Model(s) Used




# Future Work

1) Need to bring some improvemrnt in the data cleaning methods through standardised scaling non object variables.
2) Merging more classes for analysis (eg medication consumption rate, other mineral components comsumed etc).
3) Check for multicollinearity between parameters for significance.
