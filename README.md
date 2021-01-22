# Predicting_Saves
Using baseball statistics to predict saves based on past performance

## Contents
The Predicting Saves notebook contains the code for scraping URLs, scraping HTML from those URLs, and parsing them using Beautiful Soup. It goes on to clean and organize the data into dataframes before applying a number of visualization techniques for feature analysis. There are a number of models then created and tested, followed by some additional visualizations of the resulting models, error, and additional analysis. 

The Project Presentation is a PDF of a 5 minute presentation given at Metis. 

## Objective:
Build a regression model to predict the number of saves a pitcher will earn based on previous statistics

## Approach:
The features used in the final model were games finished, appearances, saves, save opportunities, holds, FIP, SO/BB, team change, BB/9, H/9, Age, two year running sum of saves, ERA+, "mistakes" per game,and batters faced per game. The training data was evaluated on simple linear regression, ridge regression, and LASSO regression models, both with the features as is and standard scaled, in order to optimize for R2 and MSE. More features were considered, created, and paired down to identify a model will higher predictive power without too much complexity. 

## Featured Techniques:
BeautifulSoup web scraping (from Baseball-Reference)
Feature Engineering & Selection
Supervised Machine Learning
Linear regression
Regularization
LASSO
Ridge regression
Exploratory Data Analysis
Data Visualizations

## Data:
Data from more than 300 pitchers and around 1500 seasons was scraped from Baseball-Reference.

## Results Summary:
A LASSO model that was based on features that was paired down through pairplots, feature interactions, and LASSO regression was chosen. The model was optimized for a combination of reducing mean absolute error and size of coefficients. The final model had a R2 of 0.41 and MAE of 10.2. In other words, our model accounts for about 41% of the variability in saves for the following year and has an average error of about 10.2 saves per prediction. The largest contributing features were considered to be in two main categories: opportunity and dominance. Further analysis should be conducted to identify future opportunity and dominance with other advanced metrics and classification algorithms. 
