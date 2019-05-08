![logo](https://github.com/ShehzadaAlam/Airbnb-Rental-Price-Prediction/blob/master/AirbnbLogo.png "Airbnb Logo")
# Airbnb-Rental-Price-Prediction:
----
The objective of this project was to model the rental prices for Airbnb apartments in London.

# Problem Statement:
----
* Airbnb is an online marketplace which allows users to post lisings on their website and it earns commissions from every booking.
* At present when someone wants to list an Airbnb rental, they have to manually analyze similar properties near their location and decide the price themselves.
* Idea of our project is to form a model to estimate what the correct price of their rental should be given the features of their property.

# Dataset:
----
* Rows: 77000+ 
* Columns: 97
* Source: [http://insideairbnb.com/get-the-data.html](http://insideairbnb.com/get-the-data.html)
----

# Data Analysis and Visualization:
----

**HeatMap:** 
![Heat Map](https://github.com/ShehzadaAlam/Airbnb-Rental-Price-Prediction/blob/master/HeatMap.png "Heat Map")

----
**Bedroom VS Price:** 
![BedroomVSPrice](https://github.com/ShehzadaAlam/Airbnb-Rental-Price-Prediction/blob/master/BedroomVsPrice.png "BedroomVsPrice")

----
**London Borough vs Price:** 
![London Borough vs Price](https://github.com/ShehzadaAlam/Airbnb-Rental-Price-Prediction/blob/master/London%20Borough%20vs%20Price.png "London Borough vs Price")

----
**ProposedSolution:** 
![ProposedSolution](https://github.com/ShehzadaAlam/Airbnb-Rental-Price-Prediction/blob/master/ProposedSolution.png "ProposedSolution")
----

## Model Creation & Selection:

**Classification metric:** 

* After feature engineering step we have created 2 bins for 'price' from 0-100 & 101-2001.
* Splitting the data into Train and Test set(70-30).
* Before performing Regression we have first done Classification to predict Price_bins. 
* We chose Random Forest and Logistic Regression because we wanted a algorithm which would allow to assign class weights to handle class imbalance problem.

![ClassificationMetric](https://github.com/ShehzadaAlam/Airbnb-Rental-Price-Prediction/blob/master/Classificationmetric.JPG "ClassificationMetric")

**Regression metric:** 
* After performing Classification on price_bins we have built XGBRegressor model for each price bin.
* We have trained the model on log transformed Target variable as price is a relative term.
* We have used L1 regularization to prevent overfitting.

![RegressionMetric](https://github.com/ShehzadaAlam/Airbnb-Rental-Price-Prediction/blob/master/Regression_metric.JPG "RegressionMetric")

----
<p>Thank You!	
<p><!-- Place this tag where you want the button to render. -->
<a class="github-button" href="https://github.com/ShehzadaAlam" aria-label="Follow @ShehzadaAlam on GitHub">Follow @ShehzadaAlam</a>
