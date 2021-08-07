# Canadian Election Study Analysis

## Overview

Selected topic:
- This project examines the Canadian Election Study, a large-scale survey conducted before and after the 2019 Canadian Federal election. In our analysis, we seek to uncover the key factors that drive Canadian voting preferences. 

Reason for selection:
- It's a rich dataset that covers a wide number of issues, and members of the group are interested in Canadian politics.

Description of source data:
- The study consists of an online survey conducted pre and post election with 37,822 respondents. The source data can be found at the [Canadian Election Study website](http://www.ces-eec.ca/). 

Question we hope to answer:
- Predict party preference based on survey data

Description of Data Exploration and Analysis Phase
- Our analysis focuses on the demographic factors and issues that influenced Canadians' voting decisions in 2019. Because of this focus, some survey questions that are closely linked to political affiliation were dropped from the dataset--for example, questions about party ID, party membership, political donations, or opinions on party leaders were not included in the dataset used in our machine learning model. Additionally, some columns that had a large number of null values were dropped from the dataset. 
- Changed our focus from predicting the exact political party to predicting wether the person was left or right leaning in the political spectrum

Our Machine Learning Model when predicting which political party you would vote for:

![Party Prediction](Resources/politicalparty.png)

Our Machine Learning accuracy when predicting if you leaned left or right on the political spectrum:

![Left-Right Prediction](Resources/leftright.png)

## Machine Learning Model

We will attempt to predict respondents' political party preferences based on their demographic information and their issue priorities. We plan to use a supervised machine learning model such as Random Forest or Ensemble Classifier to predict party preference.

- Description of data preprocessing, feature engineering and the feature selection, including the team's decision-making process
  - We removed columns with low feature importance and used get_dummies to create variables for the text columns
- Description of how data was split into training and testing sets
  - We used sklearns train_test_split function to split the data into training and testing sets
- Explanation of model choice, including limitations and benefits
  - We chose Balanced Random Forest Classifier as our machine learning model, because it allowed us to see the feature importance and because we had a large number of categorical variables our dataset was well suited to Random Forest. There's a risk of overfitting the model because of the number of features included in the survey
- Explanation of changes in model choice (if changes occurred between the Segment 2 and Segment 3 deliverables)
  - We didn't change our model but we changed our target data from many separate political parties to whether or not you were left or right leaning in the political spectrum
- Description of how the model was trained (or retrained, if they are using an existing model)
  - We used the training data from the train_test_split variables
- Description and explanation of model’s confusion matrix, including final accuracy score
  - We ended with an accuracy score of 84.6%
  - Confusion Matrix:

![Confusion Matrix](Resources/confusion_matrix.png)

## Database

Our dataset is stored in a PostgreSQL database.

## Dashboard

A Tableau Dashboard with the results of our analysis can be found here: https://public.tableau.com/app/profile/jason.hilberdink/viz/Election_Analysis/Story1.
