# Water Forecast Rodeo

This repo consists of my submissiong to the Water Supply Forecast Rodeo: https://www.drivendata.org/competitions/group/reclamation-water-supply-forecast/

A submission was not made during the submission phase since I was travelling. 

The final pipeline included preprocessing the raw inputs, performing quantile predictions using an LSTM model for the month of interest, and a post prediction Linear Regression model to estimate streams with missing values. The process is shown in the diagram below, along with the size of each of the inputs.

![image](https://github.com/quekyuchern/waterforecast/assets/40288437/25d7d34c-2fb9-49a8-8bab-a60195b2990a)

Only the months from the issue date till the season end date will be predicted. For example:
  - If the issue date is in Feb, and the season is from Apr till Jul, the monthly naturalized flows for Apr till Jul will be predicted.
  - If the issue date is in Jun, and the season is from Apr till Jul, the monthly naturalized flows for Jun and Jul will be predicted, while the actual flows for Apr and May will be used.
This means that as the issue date approaches the season end date, the range for the quantile predictions will get smaller and smaller.

Raw Data is not uploaded due to the size. The preprocessed dataset is uploaded for reference.
