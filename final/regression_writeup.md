# Car Auction Bid Linear Regression Analysis

Manveer Sadhal


## Abstract
The goal of this project was to create a linear regression model using data scraped from the car auction website [BringATrailer.com](https://bringatrailer.com/) to gain insight into the drivers of the final auction bid and offer some ability to predict the final bid for an auction given details about the particular car listed for sale as well as the listing itself. This would in turn provide a useful estimate for buyers to use as part of their bidding strategy.

Web scraping was completed using Selenium and BeautifulSoup. Data were cleaned with Pandas and NumPy. Model development and evaluation was done using SciKit-Learn.


## Design
The [BringATrailer.com](https://bringatrailer.com/) car auction site is popular with car enthusiasts, known for hosting auctions with cars that appeal to this niche demographic. The BMW M3 is one of the most popular models sold on the site. In order to help buyers avoid bidding too high, a linear regression model was developed with the intent of predicting the final bid of an auction.


## Data
### Web Scraping
Data from 1,121 auctions for the BMW M3 (model years 1994-2013) going back to Dec 2016 were scraped using Selenium and BeautifulSoup. 

### Cleaning
Nearly all of the data collected were freeform text entered by the seller, requiring significant cleaning, standardization, and categorization using Pandas. After cleaning and removing rows with missing pertinent data, 908 records remained.


## Algorithms
### Modeling
*Feature Engineering*

1. One-hot encoding categorical features
2. Log transformation of mileage

Other feature interactions and polynomial transformations were evaluated, but ultimately discarded.

At the start of modeling, 12 features were available from the scraped data.

*Models*

Ordinary least squares linear regression, Ridge regression, and Lasso regression were evaluated. The PolynomialFeatures function was used to look for additional interactions or transformations, followed by Lasso for regularization.

*Model Evaluation*

20% of the data were split as a test holdout. 5-fold cross-validation was used to evaluate candidate models using the remaining data set. Ordinary least squares, Ridge, and Lasso models performed similarly. OLS was chosen since regularization did not improve the result.

After feature engineering was completed and the model type selected, the final step was to train the model on the 80% train/validation portion of data and test on the remaining 20%.

Seven features were included in the final model, including four categorical features.

The following metrics were seen in final model evaluation:
- R<sup>2</sup>: 0.763
- Mean Absolute Error: 4377
- Root Mean Squared Error: 6585

### Visualization
Matplotlib and Seaborn were used throughout exploratory data analysis and modeling for visualization.


## Tools
- Web Scraping
    - Selenium
    - BeautifulSoup
- Data Cleaning
    - Pandas and NumPy
- Exploratory Data Analysis
    - Pandas
- Data Visualization
    - Matplotlib
    - Seaborn
- Modeling
    - SciKit-Learn


## Communication
Findings and recommendations from the modeling will be communicated during a 5-minute slide presentation.
