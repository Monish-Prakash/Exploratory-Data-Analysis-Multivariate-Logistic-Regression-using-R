# Soccer-Match-Outcome-Prediction

Soccer is a sport widely played and followed throughout Europe. We take data of 380 matches
of English Premier League for the season of 2014 across 20 teams and try to build a multinomial
logistic regression model that would predict the outcome of any match which can be win, loss or
a draw. We use team attributes related to the play styles of both teams, select relevant features
through exploratory data analysis, use feature engineering to build new features and try different
models that would give us the highest accuracy. We are able to predict the outcome with 59.65%
accuracy using a Proportional Odds Logistic Regression model which is higher than the accuracy
with which bookies who take bets on the matches can predict. </br> </br>

__Data Description:__</br>
The dataset comprised of an SQLite database with tables of matches, players and team
attributes. Below is a summary of the dataset:</br>
•+25,000 matches</br>
•+10,000 players</br>
•11 European Countries</br>
•Seasons 2008 to 2016</br>
•Players and Teams' attributes sourced from EA Sports' FIFA video game series</br>
Data obtained from: https://www.kaggle.com/hugomathien/soccer in an SQLite format.</br>

__Data preprocessing:__</br>
A subset of the data is used that consists of the Matches table joined with the Team
Attributes Table and we are only considering the _English Premier League_. Below is a snapshot
of the data we are working with:</br>
•380 observations: Since 20 teams, each playing 2 matches against every other team, we
have records of 380 matches.</br>
•18 numerical variables (on a scale of 100) represent one attribute for each team: Since
there would have been duplication of attributes, 1 for each team, we decided to take a
ratio of these attributes.</br>
•9 variables represent a ratio of an attribute for home vs. away team: After taking ratios
of corresponding attributes, we ended up having 9 attributes of form
(home_team_attribute/away_team_attribute)</br>
•1 multinomial predicted variable (win/loss/draw): Outcome of a match depends on the
number of goals score by each team. We converted the number of goals by each team
in 2 separate columns to a sinle column.</br>
•Examples of attributes: buildUpPlaySpeed_ratio, buildUpPlayDribbling_ratio,
defenceAggression_ratio, defenceTeamWidth_ratio</br>




