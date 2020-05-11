# Wrangle and Analyze Data

## Introduction
Our goal in this project is to wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations.
### Wrangling Data:
This process consists of three steps:
1. Gathering data: We have collected data from three sources:
	* The WeRateDogs Twitter archive 
	* The tweet image predictions
	* Via Twitter API
1. Assessing data: We assess the collected data to find out two different issues:
	* Quality Issues
		1. Completeness: missing data
		1. Validity: data making sense
		1. Accuracy: inaccurate data
		1. Consistency: standardization
	* Tidiness Issues
		1. Each variable forms a column
		1. Each observation forms a row
		1. Each type of observational unit forms a table
1. Cleaning data
	* Delete retweets in twitter_dogs
		1. Convert timestamp from string to datatime
		1. Convert the lowercase and invalid  names to None
		1. Delete row with the rating_denominator of an invalid value
		1. Convert rating_numerator to float
		1. Correct the inaccurate rating_numberator by extracting the correct fractional rating
		1. Change tweet_id from an integer to a string
		1. Remove the html tags from source, only keep the content inside the tags
		1. Remove underscore from breed_pred, make all title case
	* Tidiness Issues
		1. Merge the clean versions of archive, predictions, and counts dataframes
		1. Create one column for the various dog stages: doggo, floofer, pupper, puppo
		1. Extract dog breed and prediction confidence into two columns
		1. Drop unnecessary columns

For details and code, check the `wrangle_act.ipynb` notebook.

### Visualizing Data:
	* What is the monthly number of tweets?
	* What is the correlation between favorite counts and retweet counts?
	* What is the most used source for tweeting?
	* What are the most tweeted dog breeds and dog names?
	* How confident our breed predictions were?

For more details and code, check the `wrangle_act.ipynb` notebook.


