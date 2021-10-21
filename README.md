# Analyzing the Video Games Market
Rahmah Alyaseen

## Abstract
The purpose of the project is to help the game developer and publisher to understand their market. 
This will help in planing the marketing strategy and in the development decision process. 

## Design
This project originates from Data Science Bootcamps for SDAIA Academy. 
The data is provided by kaggle.com, and presents list of video games with sales greater than 100,000.
Predicting sales rate via machine learning models would enable the game developer and publisher to focuse on the important stuf.

## Data
The dataset contains 16598 video games with 16 features for each, 4 of which are categorical and A few feature highlights sales. Alongside the fields: 
Name - name of the game
YearofRelease - year which the game release
Platform - platform which can play the game
Genre - type of the game
Publisher - distributor
- Critic_score - Aggregate score compiled by Metacritic staff
- Criticcount - The number of critics used in coming up with the Criticscore
- User_score - Score by Metacritic's subscribers
- Usercount - Number of users who gave the userscore
- Developer - Party responsible for creating the game
- Rating - The ESRB ratings
- NA_Sales - sales rate in North America
- EU_Sales - sales rate in European Union
- JP_Sales - sales rate in Japan
- Other_Sales - sales rate in other countries
- Global_Sales - sum of all sales rate

## Algorithms
*Feature Engineering*
1. Mapping the correlation of columns and chose the target acording to values. 
2. Converting categorical features to binary dummy variables

*Models*
  
Linear Regression to predact thr sale rate according to critical score. 
random forest classifiers, and xgboost which settling on as the model with strongest cross-validation performance to prdact salse rate acording to feature platform and gener.
*Model Evaluation and Selection*
  
The entire training dataset of 59,400 records was split into 80/20 train vs. holdout, and all scores reported below were calculated with 5-fold cross validation on the training portion only. Predictions on the 20% holdout were limited to the very end, so this split was only used and scores seen just once.

The official metric for DrivenData was classification rate (accuracy); however, class weights were included to improve performance against F1 score and provide a more useful real-world application where classification of the minority class (functional needs repair) would be essential.

**Final random forest 5-fold CV scores:** 99 features (7 numeric) with class weights
   - Accuracy 0.797
   - F1 0.791 micro, 0.679 macro
   - precision 0.792 micro, 0.722 macro
   - recall 0.797 micro, 0.658 macro

**Holdout** 
   - Accuracy: 0.802  
   - F1: 0.795 micro, 0.685 macro  
   - Precision: 0.796 micro, 0.725 macro  
   - Recall: 0.802 micro, 0.664 macro
## Tools
- Numpy and Pandas for data manipulation
- Scikit-learn for modeling
- Matplotlib and Seaborn for plotting
- Tableau for interactive visualizations
## Communication
