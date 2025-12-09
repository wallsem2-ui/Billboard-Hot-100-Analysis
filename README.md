# 309-Final-Exam

My dataset is from the Billboard Hot 100 Number Ones Database, found on TidyTuesday in Github. 
The data covers every number one song from August 4, 1958 to January 11, 2025. The data was cleaned and filtered and the analysis looks at the number one songs from 2000-2025.

Predictor Variables:
- Length of song (length_sec) - length of the song in seconds
- Year (date) - year taken from the date variable, date of the first week the song hit number one
- BPM (bpm) - beats per minute, taken from Spotify
- Overall rating (overall_rating) - mean of three rating scores from expert judges, 1-10 scale
- Happiness (happiness) - happiness measure on 0-100 scale, taken from Spotify

Response Variable: Weeks at Number One (weeks_at_number_one) - total number of weeks the song held the number one spot, includes consecutive and nonconsecutive weeks

Other Variables:
- Song
- Artist

My visuals use scatterplots, line graphs, trendlines, and more to examine the relationship between variables. I then created 5 models to predict the number of weeks a song stayed at number one. 

When comparing the results given by the models dataframe, as well as looking visually at MAE and RMSE, there are a few models that stand out. I believe the best model to go with is the Random Forest model (model 4). Model 4 has the lowest MAE (2.64), meaning it has the smallest average error. It also has It is also on the lower end of RMSE (3.479). Although the linear models have slightly lower RMSE (3.455 and 3.471), they are very close. Additionally, all the models are pretty close in Rsquared values, so even though it is not the highest, the amount of variance explained by model 4 is comparable to the other models (and is a lot higher than the KNN model).

Implications of predictions: The rsquared values are low for every model, meaning that it is hard for models to predict the number of weeks a song will spend at number one based on these predictors. This likely implies that the response variable is highly variable and is difficult to predict. This makes sense because sometimes the qualities that make songs popular (and likely to stay at number one) are not able to be captured. However, the random forest model is the most accurate. When looking at the test dataset and comparing the actual number of weeks to the predictions, although not super accurate, the random forest model is sometimes one of the closest predictions.

Overall, when exploring the relationships contributing to number of weeks at number one and the accuracy of models in predicting this, a lot of insights can be found. We find that even though there are some moderate correlations between the variables, it is very challenging to predict the number of weeks based on any predictor. However we see that as happiness and bpm increase


