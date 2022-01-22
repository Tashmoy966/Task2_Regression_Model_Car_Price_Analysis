# Problem Statement
A Chinese automobile company Geely Auto aspires to enter the US market by setting up their manufacturing unit there and producing cars locally to give competition to their US and European counterparts.

They have contracted an automobile consulting company to understand the factors on which the pricing of cars depends. Specifically, they want to understand the factors affecting the pricing of cars in the American market, since those may be very different from the Chinese market. The company wants to know:

* Which variables are significant in predicting the price of a car
* How well those variables describe the price of a car

# Dataset
The dataset used is the [CarPrice Prediction MLR+RFE+VIF](https://www.kaggle.com/hellbuoy/carprice-prediction-mlr-rfe-vif/notebook#Step-6:-Building-a-Linear-Model) from Kaggle. 

**The 6 class labels are:**

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

Drug (object or categorical)

**Drug** refer to the type of drug consumed (through medication or direct injection) 

**Type:**

A,B,C,X,Y

# Model(s) Used

1. **KNN Classifier**

In this kernel, parameters of KNN Algorithm are described and effects of these paremeters on result are observed. First prediction is predicted with default parameters and      this   result is used for comparing. After that, best value of every parameters are found and are discussed their effects on result.Finally, GridSearch algorithm is used to find best values of each parameters. So results can be compared each other in the conclusion part.

i) Calculate distance

ii) Find closest neighbors

iii)Vote for labels

![image](https://user-images.githubusercontent.com/87931949/149998804-2881e277-abfa-4867-a354-0f40f5b0b13b.png)

[Refer](https://www.datacamp.com/community/tutorials/k-nearest-neighbor-classification-scikit-learn)

2. **Random Forest**

The Random forest or Random Decision Forest is a supervised Machine learning algorithm used for classification, regression, and other tasks using decision trees.
The Random forest classifier creates a set of decision trees from a randomly selected subset of the training set. It is basically a set of decision trees (DT) from a randomly selected subset of the training set and then It collects the votes from different decision trees to decide the final prediction.

![image](https://user-images.githubusercontent.com/87931949/149999578-242ca37e-9877-445e-a104-3c9f3baf9e68.png)

Based on the MSE the entropy of the system is reduced to get the best classification.

[Refer](https://www.upgrad.com/blog/random-forest-classifier/)

3. **SVM Classifier**

**Support Vector Machines**

Generally, Support Vector Machines is considered to be a classification approach, it but can be employed in both types of classification and regression problems. It can easily handle multiple continuous and categorical variables. SVM constructs a hyperplane in multidimensional space to separate different classes. SVM generates optimal hyperplane in an iterative manner, which is used to minimize an error. The core idea of SVM is to find a maximum marginal hyperplane(MMH) that best divides the dataset into classes.

i) Generate hyperplanes which segregates the classes in the best way. Left-hand side figure showing three hyperplanes black, blue and orange. Here, the blue and orange have higher classification error, but the black is separating the two classes correctly.

ii) Select the right hyperplane with the maximum segregation from the either nearest data points as shown in the right-hand side figure.

![image](https://user-images.githubusercontent.com/87931949/150000093-cedb850e-4796-458c-909d-77076f506677.png)

[Refer](https://www.datacamp.com/community/tutorials/svm-classification-scikit-learn-python)


# Future Work

1) Need to bring some improvemrnt in the data cleaning methods through standardised scaling non object variables.
2) Merging more classes for analysis (eg medication consumption rate, other mineral components comsumed etc).
3) Check for multicollinearity between parameters for significance.
