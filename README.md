# dsci-100-project_template

## Introduction

Tennis is a popular sport with a long history of competitive tournaments and rankings. A player's ranking is an essential metric used to evaluate their performance and overall skill level. While several factors can impact a player's ranking, such as age, seasons played, current rank, and prize money, it can be challenging to determine the best approach for predicting a player's best rank accurately.

In this proposal, we aim to predict a tennis player's best rank based on their age, seasons played, current rank, and prize money. We plan to use K-nearest neighbor regression, a machine learning algorithm, to analyze the data and make predictions. The goal of this project is to determine whether these variables have a direct or indirect impact on a player's best rank and which ones are most influential in making accurate predictions.

To accomplish this, we will use a dataset containing information on various tennis players, including their age, best rank, prize money, current rank, and seasons played. We will use five-fold cross-validation to estimate the smallest error in our model and then evaluate the optimal parameter value using the standard testing dataset. By analyzing the data and using visualization techniques such as scatter plots, we hope to gain valuable insights into the factors that influence a player's ranking in tennis.

## Predicting a Tennis Player's Best Rank Based on Their Age, Seasons Played, Current Rank, and Prize Money

 For our project we chose the columns Age, Best Rank, Prize Money, Current Rank, and Seasons. We are trying to predict the Best Rank using the other 4 variables. These predictors were selected because they contain the most data compared to other columns which mostly contain N/As. The choice of predictors was also based on their relevance to predicting a player's Best Rank. Variables such as Age, Best Rank, Prize Money, Current Rank, and Seasons were selected as they have a direct or indirect impact on a player's performance and ranking. Other variables such as Nicknames or Web Site were deemed irrelevant as they are not likely to have a significant influence on a player's ranking.

### Methods

We plan on Using K-nearest neighbor regression since all of the variables we selected are quantitative. We will have to standardize the data and determine the number of neighbors depending on the smallest estimated error which we will determine from the five fold cross validation from our tennis_data_train dataset. We will evaluate the optimal parameter value for our model by using the standard testing dataset to calculate the standard error, we will do this to all of our variables to ensure we have sufficient amount of predictors.

We will use similar scatter plots as the ones above with our standardized data, the predictors will be on the x-axis of their individual plot and the predicted Best Rank will be on the y-axis.

### Resutls

Using K nearest neighbors algorithm we compared the models for predicting the best rank of a tennis player's with multiple predictors such as their Age, Current Rank, Seasons Played, and the Prize Money they have won. In order to get the most accurate model we found the optimal number of neighbors to use for each model by performing 5 fold cross validation. Then we calculated the RMSPE of each model and then compared them. As we had expected the final model with all 4 predictors gave the most accurate result when predicting best rank.

As it can be seen in figure 3.1, Age and Seasons Played both have a weak negative relationship with Best Rank. This is confirmed by our findings using the RMSPE value as the models using only Age and Seasons Played had higher values compared to the other individual predictors and our final model. Prize money and Best Rank have a strong negative exponential relationship which was also observed in our RMSPE findings, as it had a similar RMSPE value to our final model which was the most accurate. This makes sense because a player's earnings would be directly impacted by their rank. Moreover, Current Rank and Best Rank have a positive relationship. The RMSPE value for the model using Current Rank is in between the final model and the Age model which indicates that this predictor alone would also not be the most accurate. The RMSPE value for the final model (49) although acceptable, was higher than expected, which could be due to the absence of better predictors; if this were the case, the model could be improved by considering more/alternate predictors such as player's injury history.

These findings provide insights into the relative importance of different predictors in determining a tennis player's Best Rank. The results suggest that considering all four predictors together provides a more accurate prediction compared to using them individually. Although Prize Money and Best Rank have a strong relationship, alone it does not prove to be a good predictor because Best Rank is not determined by the Prize Money, Prize Money is determined by the rank.

The findings are also useful for players, coaches and recruiters to plan and predict a player's future potential based on their current standing in the league. For players, it brings valuable insights as it would help them understand where they are in their career and motivate them to aim for higher ranks. Because Prize Money increases exponentially as rank increases (gets closer to zero) as it can be seen in figure 2.3, this model can help them understand their potential career earnings.

Overall, these findings provide potential opportunities for a continuation of research into predicting ranks for both tennis players and other athletes. It can also contribute to a more meaningful and better understanding of what factors impact a player's career and rank and provide a better understanding of the dynamics of single player sports.

### References

"Player Stats for Top 500 Players" from: 
 https://www.ultimatetennisstatistics.com/

