# Car Auction Bid Linear Regression Analysis

Manveer Sadhal


## Abstract
The goal of this project was to create a linear regression model using data scraped from the car auction website [BringATrailer.com](https://bringatrailer.com/) to gain insight into the drivers of the final auction bid and offer some ability to predict the final bid for an auction given details about the particular car listed for sale as well as the listing itself. This would in turn provide a useful estimate for buyers to use as part of their bidding strategy.

Web scraping was completed using Selenium and BeautifulSoup. Data was cleaned with Pandas and NumPy. Model development and evaluation was done using SciKit-Learn.

## Design
The [BringATrailer.com](https://bringatrailer.com/) car auction site is popular with car enthusiasts, known for hosting auctions with cars that appeal to a niche demographic. The BMW M3 is one of the most popular models sold on the site. In order to help buyers avoid bidding too high, a linear regression model was developed with the intent of predicting the final bid of an auction.


## Data
### Web Scraping
Data from 1,121 auctions for the BMW M3 (model years 1994-2013) going back to Dec 2016 were scraped using Selenium and BeautifulSoup. 

### Cleaning
Nearly all of the data collected were freeform text entered by the seller, requiring significant cleaning, standardization, and categorization using Pandas. After cleaning and removing rows with missing pertinent data, 908 records remained.

## Algorithms
*Feature Engineering*
1. One-hot encoding categorical features
2. Log transformation of mileage

Other feature interactions and polynomial transformations were evaluated, but ultimately discarded.

*Models*
Ordinary least squares linear regression, ridge regression, and lasso regression were evaluated. The PolynomialFeatures function was used to look for additional interactions or transformations, followed by lasso for regularization.

*Model Evaluation*
5-fold cross-validation was used to evaluate candidate models. 

### Visualization

### Modeling
K-fold cross-validation was used to evaluate candidate models and feature engineering.


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

