---
layout: post
title:      "Interpreting your Data"
date:       2019-04-08 12:21:05 +0000
permalink:  interpreting_your_data
---


Going through the first project in Flatiron’s Data Science program, you really get a taste of how nuanced all data science work can be. There’s many ways anyone can go about with structuring their process, and even within that process there are an infinite amount of ways to interpret what you’re looking at. I wanted to write about one instance in this project, working with the King County housing data set, where you start with a process and by following the data bread crumbs you’re able answer real world questions.

Going through the OSEMiN model, we begin by obtaining our data set of about twenty thousand houses in the King County, Washington area. The data set itself wasn’t too complicated to work with—much of the data being easy to interpret correctly on first glance. Our data was provided to us so there wasn’t much creative direction in this particular project at this step, but be prepared moving forward being comfortable querying data from a database or sometimes generating your own data.

Following through with the OSEMiN model, I was experimenting with different ways to scrub the data. Understanding there wasn’t a long list of features for this particular data set, I decided to go through each variable and independently confirm the data was “good enough” to pass an initial scrubbing, as the OSEMiN model is a fluid model allowing a “back and forth” approach to each step. On this first step – with the first variable -- I was struck by an interesting discovery. Checking for unique variables within house id’s led to a finding that there were multiple instances of each house id riddled throughout the dataset. Most of these entries were the same, some missing entries for different features, but otherwise they were undeniably the same house. The only main difference was each house was sold at a different date for a different price. I immediately began shifting towards the third step in the OSEMiN process, understanding what the data actually means, but held off to complete the initial scrubbing of the rest of the data set.

Moving onto the third step of the model, I began exploring more in this relationship between the price a house was sold for and when the house was sold. The exploratory step allows for questions outside the scope of the project to be explored and to potentially set up further questions the end model could attempt to predict. I began the exploration into this relationship by removing the “ID” assigned to each house instance. My focus was to gain insight on a pattern of monthly pricing trends, regardless of housing similarities or differences. I chose to focus on a monthly trend vs a yearly one because the data only covered houses sold between 2014 and 2015.

On the final step of this particular exploration, I wanted to reduce as many non-random variables as I could. One thing I recognized immediately is housing location can also be influenced by location type – property in central downtown real estate would vary greatly from a similar sized property in a rural suburban town. For this reason I calculated the price per square footage of each before continuing. I then plotted that price by each zipcode, used as a categorical marker to represent different areas in King County. 

This entire process was my own. There were guidelines and an understanding of what I was supposed to do with the data but from start to finish I made the choices that led me to an idea, then a question, an answer, and now more questions. We’re told “data is data, there is no right or wrong” when working with information, and being able to unpack and explore such a vast dataset really allowed to understand that.

