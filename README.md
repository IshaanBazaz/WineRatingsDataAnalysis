Hotel TULIP would like to review the menu and tempt any guest with delightful wines. The hotel’s CIO, Dr Bear Guts (not Bill Gates!), believes that ratings provided by the WineEnthusiast (a multichannel marketer of a growing line of wine) are great resources to help their Market Promotion Division to identify potential excellent wine with affordable price. Hence, Hotel TULIP would like to analyze a wine rating dataset and discover taste and price patterns of different types of wine over the world.

Two tasks were completed:

## Task 1 : Numeric and Categorical Value Analysis

For a data scientist, after obtaining the dataset, the first most crucial task is to obtain a
good understanding of the data he or she is dealing with. This includes: examining the
data attributes (or equivalently, data fields), seeing what they look like, what is the data
type for each field, and from this information, determining suitable numerical/visual
descriptions.
The first task is to read the json file as a Pandas DataFrame and delete the rows
which contain invalid values in the attributes of “points” and “price”.
Then, we need to answer the following two questions in our IPython notebook based
on this dataset:

(1) what are the 10 varieties of wine which receives the highest number of reviews?

(2) which varieties of wine having the average price less than 20, with the average points
at least 90? Assuming there is no duplicate review in the data, i.e., each row represent
a unique wine.


In addition, we need to group all reviews by different countries and generate a statistic
table, and save as a csv file named “statisticByState.csv”. The table must have four
columns:

Country – listing the unique country name.

Variety – listing the varieties receiving the most reviews in that country.

AvgPoint – listing the average point (rounded to 2 decimal places) of wine in that
country

AvgPrice – listing the average price (rounded to 2 decimal places) of wine in that country

## Task 2 : Text Analysis

In this task, we are required to write Python code to extract keywords from the
“description” column of the json data, used to redesign the wine menu for Hotel
TULIP.
We need to generate two txt files:

HighFreq.txt This file contains the frequent unigrams that appear in more than 5000
reviews (one row in the dataframe is one review).

Shirazkey.txt This file contains the key unigrams with tf-idf score higher than 0.4.

To reduce the runtime, first we need to extract the description from the variety of
“Shiraz”, and then calculate tf-idf score for the unigrams in these descriptions
only.
In both txt files, all unigrams are sorted alphabetically and are saved line by line
without duplicate. Before we calculate the unigram frequent or tf-idf, we need to
remove the stop words in all description using the provided “stopwords.txt” or using
the built-in function in Python.
