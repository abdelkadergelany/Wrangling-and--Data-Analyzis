# Wrangling and  Data Analyzis
 1- Introduction

In this project called Data Preparation and Analysis, we had to collect data from various sources and various formats, evaluate their quality and order, and then clean them using Python and its libraries. The dataset we processed is the archive of tweets from the Twitter user dogrates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people’s dogs with a humorous comment about the dog.

2- Steps

Our work was performed in 5 steps:
 Step 1: data gathering
 Step 2: data evaluation
 Step 3: data cleaning
 Step 4: data storage
 Step 5: Analyze and visualize the data

3- Data gathering

In this step, we gathered 3 datasets.We gathered the Twitter archives of WeRateDogs under the dataset twitterarchivedf using the readcsv method of pandas. After that, we collected the image predictions of the tweets in tsv format using the library request. Subsequently, using the tweet IDs in the WeRateDogs Twitter archive, we queried the Twitter API to get the JSON data for each tweet using Python’s Tweepy library and store the JSON data set for each tweet in a file called tweetjson.txt. From this tweetjson.txt, we extracted the number of retweet and favorite for each tweet in the Twitter archives of WeRateDogs.

4- Data evaluation

After collecting the three data elements, we made the evaluations visually and programmatically for the quality and tidiness problems.

5- Data cleaning
We detected and documented at least eight (8) quality problems and four (4) tidiness problems.

5.1- Quality Problems
  1. Presence of retweets in the archive data frame which is of no interest to      our analysis.
  2. The data type of in reply to user id, in reply to status id are in float
  3. The data type of in reply to user id, in reply to status id are in float
  4. timestamp data type should be modify to date time
  5. Record with rating denominator less or greater than 10. This constitute      an incoherence with reference to the rater documentation
  6. Record with rating numerator less than 10 or too high since these are      probably outliers
  7. Presence of HTML tags in source column.
  8. Some names starting with lower case instead to start with capital case 2.

5.2 Tidiness Problems

  1. Since we decided to drop retweets, we should remove retweeted status id,    retweeted status user id and retweeted status timestamp columns from    twitter archive df.

  2. The columns floofer, pupper, doggo and puppo should be merged into    twitter archive df as stage columns and should have as data type category     since their value is just limited to 4 possibilities.

  3. Join the columns retweet count and favorite count from df status to    twitter archive df for a better data nalysis.

  4. p1 conf,p2 conf,p3 conf can be used to evaluate how weel the deep    learning prediction algorithm performs, so, so these columns should be    added to twitter archive df For tha analysis and visualisation, confere act    report.pdf


 6 Conclusion
   We were able to complete all of these steps in accordance with what we learned in the classroom in terms of data quality and tidiness. The most difficult step was querying the tweeter API using the Tweepy library. This took about 30 minutes to complete. In the future, we would like to explore other data collection techniques, such as web scraping.
