# ML_Football_game_prediction
Data Analysis
Ultimate 25k+ Matches Football Database

Objectives for this Part

* Practice identifying opportunities for data analysis, raising hypothesis, and formulating research tasks.
* Practice performing EDA, statistical inference, and prediction.
* Practice working with SQL datasets.
* Practice visualizing data.
* Provided dataset: https://www.kaggle.com/prajitdatta/ultimate-25k-matches-football-database-european

Requirements:

* Perform data cleaning and feature engineering. Work with features - handle missing data if needed, use SQL and Pandas functions to create other additional features.
* Perform exploratory data analysis. Describe the data with basic statistical parameters - mean, median, quantiles, etc. Use parameters that give you the most important statistical insights of the data. Grouping the data and analyzing the groups - using SQL or Pandas aggregate methods. Visualize the data - you can use line, scatter, histogram plots, density plots, regplots, etc.
* Perform statistical inference. Raise and test statistical hypotheses. Set appropriate significance levels and create confidence intervals for the variables of interest.
* Train linear machine learning models and use them for forecasting. Use cross validation, information criteria, and/or other methods to specify your models correctly. Choose and use appropriate metrics to measure your models' performance.
* Create a Google Data Studio dashboard with at least three different types of charts.
* Provide clear explanations in your notebook. Your explanations should inform the reader what you are trying to achieve, what results did you get, and what these results mean.
* Present the project - the data, methods, and results.
* Provide suggestions about how your analysis can be improved.
  
Used Libreries:

Numpy; Pandas; Sqlite3; Matplotlib; Seaborn; Scipy.stats; Sklearn; xml.etree.ElementTree

Findings:

* Different data tables and additional data were not collected in the same periods (e.g. team attributes were filled in from 2010 on).Therefore, all calculations and assumptions were made only for this period.
* The 11 leagues play a different number of matches and the number of teams participating in the championships is different. By 2015, as many as 4 countries have 20 teams playing in each league, with the smallest number of teams in the Swiss league - 10. Over the whole period (2008-2016), the countries with the most teams played 3,040 matches each (380 per season).
* The aim of the paper was to find the features that allow to predict the match result using LinearRegression and LogisticRegression models.
* The focus was on the details of the team and the match. FC Barcelona has been the most successful club both home and away (most wins).
* The details and physical characteristics of the players were not focused on because the data does not reveal what time the player was on the field, how much he spent playing, so that I could confidently state his contribution to the successful end of the match. This task could be for the future.
* The general and clear observation is that a team has a better chance of winning when playing in its own stadium (as shown by the plots and hypothesis). The result of a drawn match is meaningful compared to the probability of an away win, i.e. a draw is more likely than an away win. In this case, the home team scores between [2.44, 2.49] goals against the visitors. The visitors team scores between [1.16, 1.19] goals.
* The prediction of the result was carried out in 3 steps: selecting the numerical properties of the team and the match, selecting the categorical properties and carrying out module on each group separately. In the last step, the two groups were combined and a joint modeling was performed with the following conclusions:the model's performance evaluation indicates that there is room for improvement. The accuracy, precision, recall, and F1 score are relatively low, indicating that the model may not be capturing the underlying patterns and relationships in the data effectively. The final accuracy score of 0.461 indicates that the model correctly predicts the class of approximately 46.1% of the instances in the test set.
