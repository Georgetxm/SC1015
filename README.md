# SC1015 Mini-Project - Estimating Time of Food Delivery

## About 
This is the mini project for SC1015 - Introduction to Data Science and Artificial Intelligence (DSAI). We performed analysis on the estimated time for food delivery [dataset](https://www.kaggle.com/datasets/gauravmalik26/food-delivery-dataset?select=train.csv) from Kaggle.

#### Members
- Teo Xuan Ming
- Lim Yan Xuan
- Pascalis Pandey


### Problem Motivation
With online orders increasing since the pandemic, customers want to know when their orders will arrive, and they expect those estimates to be as precise as possible. Inaccurate delivery time estimates can cause customer dissatisfaction, leading to negative ratings and lost business for the delivery platform.

### Problem Definition
- Can we predict the estimated time of delivery based on the delivery rider's attributes?
- Are we able to identify any biases in ratings without factoring in performance metrics like delivery timings?

### Resources (found in this folder)

- [Original Dataset](https://github.com/Georgetxm/SC1015/blob/main/train.csv)
- [Cleaned Dataset](https://github.com/Georgetxm/SC1015/blob/main/train_cleaned.csv)
- [Presentation Slides](https://github.com/Georgetxm/SC1015/blob/main/SC1015-MiniProj.pdf)
- Video can be assessed from this [link](https://www.youtube.com/watch?v=ZABvxkkY4mM)

### Walk-Through
1. [Data Preparation and Cleaning](https://github.com/Georgetxm/SC1015/blob/main/Data_Preparation_Cleaning.ipynb)
2. [Exploratory Data Analysis, Data-Driven Insights & Recommendations](https://github.com/Georgetxm/SC1015/blob/main/Exploratory_Data_Analysis.ipynb)
3. [Machine Learning Techniques to solve the problem](https://github.com/Georgetxm/SC1015/blob/main/Machine_Learning_without_distance.ipynb)
4. [Machine Learning with engineered feature: distance](https://github.com/Georgetxm/SC1015/blob/main/Machine_Learning_V2_w_distanceipynb)

    We have 2 notebooks showcase the differences of our models with and without the engineered feature. Please use [4](https://github.com/Georgetxm/SC1015/blob/main/Machine_Learning_V2_w_distanceipynb) to grade us as 3 is merely to showcase our thought process.

### Conclusion
- Answering our sub-problem, we are unable to find any relation between ratings and other categorical features. Hence, we conclude that there are no biases in ratings.
- Factors that could affect **Delivery Time** includes:
    - Numerical Columns 
        - Distances, Multiple deliveries and age. (Positive Correlation)
        - Ratings (Negatively Correlated)
    - Categorical Features 
        - Traffic Density
        - City Terrain 
        - Weather
    
- The XGBoost model we implemented to estimate delivery time has a 79% accuracy with a marginable error of estimation of just 18.
- From our findings, we can suggest that to reduce the delivery time, the algorithm can be further optimised such that it minimises delivery distances between a user and the nearest restaurant. Secondly, allow the users to prioritise their deliveries through a greater fee to ensure that the deliverer is only delivering his/her order. Lastly, for users to avoid peak lunch hours like 12pm to 2pm and dinner period like 5pm to 8pm for faster deliveries. 

### Key Learning Points
1. Using Plotly as a tool for interactive visualisation
2. Deriving distance from latitude and longitude coordinates, using the haversine formula
3. Feature engineering (engineering Distance and DeliverySpeed)
4. Performing ANOVA test and SelectFromModel for feature selection
5. Implementation of XGBoost, Lasso Regression, Random Forest Regressor, and Grid Search Cross Validation

### Contributors

### References
1. [Data-to-Viz](https://www.data-to-viz.com/)
2. [Outliers: Keep or Drop](https://towardsdatascience.com/outliers-keep-or-drop-892b599b8ab6)
3. [Guidelines for removing outliers](https://statisticsbyjim.com/basics/remove-outliers/)
4. [Regularisation in Machine Learning](https://towardsdatascience.com/regularization-in-machine-learning-76441ddcf99a)
5. [L1, L2 Norm and Regularisation](https://www.analyticssteps.com/blogs/l2-and-l1-regularization-machine-learning)
6. [Random Forest Regression](https://towardsdatascience.com/random-forest-regression-5f605132d19d)
7. [Lasso Regression](https://www.mygreatlearning.com/blog/understanding-of-lasso-regression/#:~:text=Lasso%20regression%20is%20a%20regularization,i.e.%20models%20with%20fewer%20parameters)
8. [Introduction to XGBoost Algorithm](https://www.analyticsvidhya.com/blog/2018/09/an-end-to-end-guide-to-understand-the-math-behind-xgboost/)
9. [XGBoost Algorithm](https://towardsdatascience.com/https-medium-com-vishalmorde-xgboost-algorithm-long-she-may-rein-edd9f99be63d)
10. [Exploratory Data Analysis : A Beginners Guide To Perform EDA](https://www.analyticsvidhya.com/blog/2021/06/exploratory-data-analysis-a-beginners-guide-to-perform-eda/)
