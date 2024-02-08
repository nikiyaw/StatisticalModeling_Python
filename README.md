# Statistical Modelling, Analyzing Cafes around Bike Stations

## Overview
The goal of this project is to study the relationship between bike stations and the number of cafes around the bike stations. Data are obtained through APIs from CityBikes, Foursquare and Yelp.

## Tools and Programming Language(s)
API, Jupyter Notebook, Python

## Process
1. Obtain data through API integration from CityBikes, Foursquare and Yelp.
2. Perform data cleaning and data wrangling on the raw data. 
3. Merge all the clean datasets.
4. Study the relationship between the number of cafes near the vicinity of the bike stations.
5. Build linear regression models (totalBikeSlots vs. F_numberOfCafes & totalBikeSlots vs. Y_numberOfCafes) to test the hypothesis.

## Results
totalBikeSlots vs. F_numberOfCafes
The model is capable of explaining only 69.6% of the patterns in the data. The regression output shows a p-value of 0, which indicates the F_numberOfCafes does impact the totalBikeSlots. The coefficient value of 1.1229 shows that the increase of F_numberOfCafes will have a positive impact on the totalBikeSlots.

totalBikeSlots vs. Y_numberOfCafes
The model is capable of explaining only 45.9% of the patterns in the data. The p-value is 0.001, which means that the F_numberOfCafes does impact the totalBikeSlots. The coefficient value of 0.8753 shows that the increase of F_numberOfCafes will have a positive impact on the totalBikeSlots.

After conducting a t-test to investigate if the results are similar, it shows that the data are nearly identical.

## Challenges 
1. Fairly small data sample is obtained
2. Huge amount of null values are found in interested variables (ratings)
The inital plan was to also study the ratings for the cafes but there are too many null values in the data obtained using the Foursquare API. To avoid making over-arching assumptions, the rating variable is dropped due to lack of information. 

## Future Goals
1. Obtain a bigger sample size.
2. Since the CityBikes app is providing real-life data, it would be interesting to explore different time periods. 

