# Water Forecast Rodeo

This repo consists of my submissiong to the Water Supply Forecast Rodeo: https://www.drivendata.org/competitions/group/reclamation-water-supply-forecast/

A submission was not made during the submission phase since I was travelling. 

The final pipeline included preprocessing the raw inputs, performing quantile predictions using an LSTM model for the month of interest, and a post prediction Linear Regression model to estimate streams with missing values. The process is shown in the diagram below, along with the size of each of the inputs.

![image](https://github.com/quekyuchern/waterforecast/assets/40288437/25d7d34c-2fb9-49a8-8bab-a60195b2990a)

