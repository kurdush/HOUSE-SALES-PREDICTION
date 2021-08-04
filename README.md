# HOUSE-SALES-PREDICTION
* The goal for this project is to build an end to end solution or application that is capable of predicting the house prices better than individuals. Another motivation for this project is to implement similar solution at my workplace and help Investments and Residential team make data driven decisions.
* here the object is to discuss the major factors that affect housing price and make precise predictions for it. We use 22  explanatory variables including almost every aspect of residential homes in King county, Usa.
*  Methods of both statistical regression models and machine learning regression models are applied and further compared according to their performance to better estimate the final price of each house. 
*  The model provides price prediction based on similar comparables of people’s dream houses, which allows both buyers and sellers to better negotiate home prices according to market trend.

 - - - -
 
 ## Data Source
 * https://www.kaggle.com/harlfoxem/housesalesprediction 
 * https://nominatim.openstreetmap.org/search/  
 ---------------------------------------

## Terms that are mainly used in project
 
* ### Preprocessing
   \- Data preprocessing is a process of preparing the raw data and making it suitable for a machine learning model. It is the first and crucial step while creating a machine learning model.

* ### Regression:
   \- Regression in machine learning consists of mathematical methods that allow data scientists to predict a continuous outcome (y) based on the value of one or more predictor variables (x). 
   
   \- Linear regression is probably the most popular form of regression analysis because of its ease-of-use in predicting and forecasting.

* ### Heat map:
   \- A heat map is a two-dimensional representation of information with the help of colors. Heat maps can help the user visualize simple or complex information.

* ### KDE plot:
   \- KDE Plot described as Kernel Density Estimate is used for visualizing the Probability Density of a continuous variable. 
   
   \- It depicts the probability density at different values in a continuous variable. We can also plot a single graph for multiple samples which helps in more efficient data visualization.
   
* ### Residual plot:
   \- A residual is a measure of how far away a point is vertically from the regression line. Simply, it is the error between a predicted value and the observed actual value.
   
* ### Pipeline:
   \- A machine learning pipeline is used to help automate machine learning workflows. 
   
   \- They operate by enabling a sequence of data to be transformed and correlated together in a model that can be tested and evaluated to achieve an outcome, whether positive or negative.
   
---------------------------------------

## Visualizations 
 * ### CountPlot
    ![Alt text](https://github.com/kurdush/HOUSE-SALES-PREDICTION/blob/7a99ef4b580dc5ae87a026a24082181b22965193/Images/count_plot.png)
    
    \- The above graph is Count plot between bedrooms,bathrooms,floors and grade. We use countplot rather scatter plot for easy understanding.
    
* ### Scatter Plot Matrix
   ![Alt text]()
   
   \- These are  scatter plots for all the sqft area columns with respect to price. It is used here to observe and show the relationship between numerical values. In the above plots , dots represents actual data points.
   
 
 * ### Regression Plot
    ![Alt text]()
    
    \- Regression plot for the above four scatter plots. The linear line is the predicted one.
 
 * ### Heat Map
    ![Alt text]()
    
    \- This is a heatmap is drawn only between selected columns which are having high correlation values. 
 
 * ### KDE plot for price vs probability density function
    ![Alt text](https://github.com/kurdush/HOUSE-SALES-PREDICTION/blob/8367dd7b131cbf18e527687a84979346fe5a9e5e/Images/KDE_plot_for_price_vs_probability_density_function.png)
  
 * ### Residual plot for price vs probability density function.
    ![Alt text](https://github.com/kurdush/HOUSE-SALES-PREDICTION/blob/2cb057bfaae208efdaf191c375b5d2dead9088d1/Images/Residual_plot_for_price_vs_probability_density_function.png)
    
 * ###  final regression plot which got accuracy upto 80%
    ![Alt text]()
    
  

   

   
   




