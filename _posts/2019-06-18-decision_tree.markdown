---
layout: post
title:      "Decision Tree"
date:       2019-06-18 13:50:23 -0400
permalink:  decision_tree
---


Module 3 introduced machine learning concepts that were more powerful that the regression analysis techniques we’ve been working with thus far. For our final project for this module, we were tasked with completing a predictive analysis of our choice.

The Black Friday dataset was a lengthy file containing a plethora of customer information collected by a shop to be able to predict shopping patterns for black Friday. It contained about 500,000 rows of data and multiple categories such as the customers age, gender, and the products they purchased.

After we imported our dataset into our jupyter notebook, we had to scrub and explore the data. The data wasn’t too messy, we noticed there were some missing values that were easily remedied. Exploring our data we made some observations. A quick bar graph of purchases grouped by gender revealed there were almost 3 times as many purchases made by males compared to females. Next we compared average transactions by each age group. Although ages 26 to 35 made the most number of transactions, the average purchase amount was similar between all age groups. After that we compared the different city categories. This feature was left vague from the dataset, but we were able to assess that it meant the socioeconomic area the customer lived (Upper, Middle, or Lower class). We I compared the 3 different categories and noticed that city category B had the greatest number of purchases. Lastly, we created a bar graph measuring the number of customers with different occupations, separating the information between men and women of each occupation. We noticed a disparity between common occupations found between customers, most of which we’re similar between most common for men and for women.

In the final section we decided to create a decision tree for classification, scikit-learn. The resulting decision tree would be able to accurately predict the gender of the customer. To begin, we made sure to encode our categorical features as numbers. There are helpful object in sklearn’s “preprocessing” module to help with that, such as “LabelEncoder” for features in a binary format and “OneHotEncoder” for nonbinary features. Once the data was properly encoded, we split our data into training and testing sets. This was accomplished by passing the predictors and target feature to the “train_test_split” function, to create a train test split. After our training data and testing data were separated, we created an instance of the classifier with any parameter value, and then fit our data to the model and made our predictions using .fit() and .predict(). Our model is now trained and generated certain predictions. We tested this trained model against our testing set, and using an accuracy measure and confusion matrix we were able to achieve 99% accuracy with our model.

