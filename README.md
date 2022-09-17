# We-Rate-Dogs-Data-Analysis-Project
INTRODUCTION
This report summarises the wrangling and analysing of data of 5000+ tweets from WeRateDogs Twitter account, gathered from a variety of sources and in a variety of formats. The quality and tidiness was assessed, and then cleaned. Some insights were revealed and visualizations to aid better understanding.

DATA GATHERING
In this project the data was gathered from three different sources:

The first dataset was provided beforehand by Udacity (twitter_archive_enhanced.csv), so it was downloaded and imported manually into the jupyter notebook by using the pandas "read_csv" function.
The second dataset(image-predictions.tsv) was downloaded programatically using the request library, it was then read into the jupyter notebook using the pandas "read_csv" function again although this time the delimeter had to be specified as this was a tab seperated file instead of commas like the csv file.
The third dataset(tweet-json.text) was to be gathered from Twitter's API using Tweepy. Unfortunately i was not granted access by Twitter so i used the alternative method which was the txt file provided by Udacity. It was then run line by line into a pandas dataframe.
DATA ASSESSMENT
In this project the datasets were assessed in two ways;

Visual
Programmatical
The data was visually assessed by looking through each dataframe critically. The data was assessed programatically using several pandas functions such as info, head and describe to take a deeper look into the data so we can see the quality and tidiness issues and then address them. Several issues were discovered and they are listed below:

Quality issues
The datatype of the "tweet_id" column is integer and should be object.
Some of the dog names in the 'p1_conf', 'p2_conf' and 'p3_conf' columns aren't consistent as some start with upper case while the other are all in lowercase.
The "timestamp" column data type is an object instead of a datetime data type.
Rating denominator not constant and outliers in rating numerators.
Retweets are included in the dataset.
Drop in_reply_to_status_id, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id and retweeted_status_timestamp as they have too many missing values.
The "source" column is ambiguous.
Inconsistent use of lowercase and uppercase and underscores in p1, p2,p3 columns
Creating year and month columns from timestamp and dropping timestamp.
Tidiness issues
The 'doggo', 'floofer', 'pupper' and 'puppo' columns should all be combined. The observations are recorded as variables instead of values.
Merge the dataframes df1, df2, and df3 as the datasets are part of the same observational unit.
DATA CLEANING
The data cleaning phase is where the tidiness and quality issues of the datasets were tackled using several pandas functions and methods, using for loops and also numpy functions to make sure the final product is sufficient enough to derive insights from. Udacity asked to look out for at least 8 quality issues and 2 tidiness issues as cleaning the whole dataset would have been too cumbersome.
