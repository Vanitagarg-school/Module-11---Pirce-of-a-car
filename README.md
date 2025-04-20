The primary goal of the analysis is to provide meaningful insights into the factors driving used car prices, aligning with the business objectives to empower the client with actionable data-driven evidence.
Jupyter notebook : http://localhost:8888/notebooks/jupyter-1.0.0/practical_application_II_starter/Price_of_used_cars.ipynb

# Data Overview:
Car dealerships aim to maximize profitability through high inventory turnover and optimal vehicle pricing. Understanding the selling price of used cars is crucial to avoid overpricing and prolonged inventory holding. 
We will use past transaction data and regression analysis to determine the key factors affecting used car prices and recommend appropriate pricing strategies.
The dataset encountered includes various characteristics of used cars such as fuel type, condition, size, type, color, price, and odometer readings. 
However, specific issues such as unrealistic and missing values were noted, especially regarding the price and odometer readings, which imply challenges that need to be addressed for a reliable analysis.

# Data Quality and Preparation Observations:
The provided data exhibited quality issues notably with numerous missing values and unrealistic entries (e.g., $0 price and 0-mileage odometer readings).
Variables such as car features like fuel, condition, size, and type were crucial for realistic data manipulation but complicated the filling of missing values.
To maintain data integrity, records with unrealistic values for price and odometer were excluded from the analysis. Additionally, features perceived as less impactful on used car prices, such as ID, VIN, State, Manufacturer, and model, were omitted.

# Data Correlations:
There is a positive correlation between price and year meaning new car has more value than the old cars. 
Similarly, there is a negative correlation between price and odometer which make sense as the vehicle will lose value if it was driven too much, and a slight negative correlation between odometer and year which depicts that old cars are more likely to be more driven.

# Data Modeling:
The modeling process was more complex than expected due to the vast volume and detailed nature of the data, which consisted of hundreds of thousands of observations and numerous polynomial features. 
Although I considered various regression models, I ultimately selected a polynomial of degree 3 due to its effectiveness and practical interpretation.
Difference in MAE for each increase in polynomial is becoming less important. The models with 2 and 3 degree polynomial are capable of capturing 81.5% and 81.6% of the variation in price.
Despite the application of L1 and L2 normalization/regularization techniques, the impact on model performance was minimal. 
The most significant determinants of price variability were found to be the vehicle's year, odometer reading, drive type, number of cylinders, and type of fuel.

# Findings:
Based on the polynomial degree 3 model, my recommendations for dealerships to maximize the selling prices of their vehicles are:
1- Year of the Vehicle: Aim for newer models as they generally fetch higher prices.
2- Odometer: Seek out vehicles with lower mileage to enhance their market value.
3- Drive: Focus on vehicles with forward or rear-wheel drive configurations.
4- Cylinders: Include vehicles with greater cylinder counts which typically command higher prices.
5- Fuel: Prefer gas-powered vehicles as they often have greater resale value.
6- Transmission: Opt for vehicles with automatic transmissions to increase their attractiveness.
By emphasizing these six criteria in inventory selection, dealerships can effectively optimize their stock. 
Nevertheless, it is crucial to recognize that this model does not take into account potential profit margins or inventory turnover rates.

