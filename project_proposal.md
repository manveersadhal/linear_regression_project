#### Manveer Sadhal
#### Sep 22, 2021

# Car Auction Price Linear Regression - Project Proposal
## Need
[BringATrailer.com](https://bringatrailer.com) is an auction website focused on enthusiast cars. A car collector has requested that a linear regression model be developed for him so that he can predict the final price of a given auction and bid competitively to get the best deal.

## Data Description
### Data
The primary source of data will be from BringATrailer.com, obtained through scraping the pages of completed auctions. The focus of this linear regression will be on one specific brand and model, the BMW M3. 

Additional information on each car based on the vehicle identification number (VIN) may also be used to verify build dates and options that the car was ordered with.

An individual sample will be data from the webpage of one completed auction.

Features:
- Mileage
- Exterior color
- Interior color
- Transmission (manual or automatic)
- Body style (coupe or convertible)
- Model year
- Location of seller
- Date sold
- Type of seller (dealer or private party)
- Number of photos included in the posting

The target of the model will be the auction sale price for a given car.

### Algorithm
A linear regression model will be created using python. The correct model will be selected and validated.

## Tools
- Web Scraping
    - BeautifulSoup
    - Selenium
- Data Cleaning
    - Pandas
- Model Development and Testing
    - scikit-learn
- Visualization
    - Matplotlib
    - Seaborn

## MVP Goal
Scrape at least 1,000 auction pages. Show that there is a relationship between the model year of the car and the final auction bid with a scatter plot.

Brief text will be included to describe findings and preliminary conclusions.