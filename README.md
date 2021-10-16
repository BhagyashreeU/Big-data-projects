# Big-data-projects

# Task 1 : **Build a word cloud of top 100 words used in NY Times articles using Apache Hadoop or Spark**

**Implementation Steps**

➢ Imported all required libraries (Pyspark, nltk, matplotlib, wordcloud)

➢ Read entire text file (NYTimes) using sc.textfile

➢ Converted all words to lower case ( lower () ) and removed stop words from the file

➢ Tokenized the words (word_tokenize) which splits each line separated by spaces into words

➢ Cleaned-up all the punctuations (string.punctualtion ())

➢ Map every token with count 1

➢ Performed aggregation of data using reducebyKey

➢ Sort in descending order ( sortbykey() )

➢ Take top 100 words (take ())

➢ Convert Key,Value pair to dictionary

➢ Form word Cloud

# Task 2: **Create the word cloud for top 5 news category that has the most of news articles.**

# Implementation Steps

➢ Read the file 'nytimes_news_articles.txt'(sc.textfile) line by line and check if the 'http://www.nytimes.com/' text exists in the line, if yes then write the same line in another file called ‘output.txt’.

➢ While writing the same line in another file, remove the URL content from the string and just retain the category part e.g. /nyregion/

➢ Map every token with count 1

➢ Performed aggregation of data using reducebyKey.

➢ Sort in descending order ( sortbykey() )

➢ Take top 100 words ( take() )

➢ Convert Key,Value pair to dictionary.

➢ Form word Cloud

# Task 3: List the top 10 words that are shared among the highest number of news articles of the same category.

# Implementation Steps

➢ Read entire text file (NYTimes using sc. textfile)

➢ If line contains 'URL: http://www.nytimes.com/' then fetch only category from URL and store it into a global category variable.

➢ If line contains other than URL then tokenize the words, convert words to lower case, remove stop words and punctuations and then join the word with category to form unique key which will of the form category#word

Ex: If the category us/politics contains word trump then following key will be formed us/politics#trump.

➢ Each such formed key is mapped with count 1

➢ Performe aggregation of data using reducebyKey.

➢ Sorted in descending order ( sortbykey() )

➢ Since the data is already sorted by descending order, fetch the most frequent word from each category until there are 10 distinct categories in the result or all categories are exhausted if there are no more than 10 distinct categories.
