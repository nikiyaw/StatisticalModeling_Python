# Final-Project-Statistical-Modelling-with-Python

## Project/Goals

In this project, we are extracting data from 3 different APIs: CityBikes, Foursquare and Yelp. 
The goal of this project is to study the relationship between bike stations (data from CityBikes) and the POI around those bike stations (data from Foursquare and Yelp). 

## Process

CityBikes API
1. Explore the data structure of the CityBikes API and understand the information provided. 
2. Choose a city of interest and further explore the data sets available. 
3. Select relevant information (latitude, longitude, number of bikes) from the chosen city and transform the data into a dataFrame. 
4. Export the dataFrame in a csv file for better access. 

Foursquare & Yelp API
1. Import the csv file from city_bike notebook. 
2. Use the information (latitude & longitude) to carry out queries. 
3. Pick a point of interest, in my case, cafes around all the bike stations. 
4. Explore the data and understand the information provided. 
5. Extract relevant data and transform them into dataFrames. 
6. Export both dataFrames in csv files for better access. 

Joining data
1. Import both the Foursquare and Yelp csv files. 
2. Merge the data and create a new dataFrame for better exploration. 
3. Study the relationship between the interested variables: totalBikeSlots, F_numberOfCafes & Y_numberOfCafes. 
4. Carry out different hypothesis testings to learn more about the data. 
5. Compare the data from Foursquare and Yelp to decide which app provides better coverage. 

Building a model
1. Build 2 linear regression models (totalBikeSlots vs. F_numberOfCafes & totalBikeSlots vs. Y_numberOfCafes).
2. Compare the results from both apps using a t-test. 
3. Interpret the findings. 

## Results

From the 2 simple linear regression models we have built (totalBikeSlots vs. F_numberOfCafes & totalBikeSlots vs. Y_numberOfCafes), the results are as follows:

totalBikeSlots vs. F_numberOfCafes
The model is capable of explaining only 69.6% of the patterns in the data. The regression output shows a p-value of 0, which indicates the F_numberOfCafes does impact the totalBikeSlots. The coefficient value of 1.1229 shows that the increase of F_numberOfCafes will have a positive impact on the totalBikeSlots.

totalBikeSlots vs. Y_numberOfCafes
The model is capable of explaining only 45.9% of the patterns in the data. The p-value is 0.001, which means that the F_numberOfCafes does impact the totalBikeSlots. The coefficient value of 0.8753 shows that the increase of F_numberOfCafes will have a positive impact on the totalBikeSlots.

Since we are obtaining data from two different sources (Foursquare, Yelp), we can conduct a t-test to investigate if the results are similar. There was a warning message that popped out, sayint that there is precision loss occurred in moment calculation due to catastrophic cancellation. This occurs when the data are nearly identical.

## Challenges 
1. Fairly small data sample is obtained
2. Huge amount of null values are found in interested variables (ratings)
The inital plan was to also study the ratings for the cafes but there are too many null values in the data obtained using the Foursquare API. To avoid making over-arching assumptions, the rating variable is dropped due to lack of information. 

## Future Goals
(what would you do if you had more time?)
1. Obtain a bigger sample size.
2. Since the CityBikes app is providing real-life data, it would be interesting to explore different time periods. 

