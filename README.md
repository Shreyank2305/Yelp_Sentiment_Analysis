# Yelp_Sentiment_Analysis
Starting with libraries pandas, numpy, matplot, seaborn, nltk
For data we are using yelp reviews, which has around 10k reviews.
Now we understand that character count or word count is a rich factor for our analysis, so in this case we are considering character count.
So we want an additional column which holds the character count of each review. 
Further we use seaborn library to plot histograms that give us insights. Here we get to see that we have more reviews with 4 and 5 stars.
Boxplot being important feature for data visulaization, is implemented but we cannot get much useful information as outliers are large in number.
We need something to be combined with text length to extract something important. Hence we go with correlation from pandas library.
For better visulization we can use heatmap, from the heat map we clearly learn about positive correlation amongst three factors and negative correlation of one factor(cool) with remaining three.
I agree with selecting reviews with either one star or five star. Clearly they will be exactly opposite of each other which can help our analysis.
Turns out that we are left with only 4086 entries with 1/5 star ratings.
Now comes the task of processing the text to make it useful. To bring it such a form that a machine can make some sense from it. Removing stopwords and punctuations. 
The idea is to get all the useful unique words and plot them or compare them with each review. CountVectorizer comes in handy. We apply it to the entire set of 4086 entries. From which we get the size of the vocabulary.
Next we simply use 30 percent of the dataset as our training dataset. And finally we use multinomial Naive Bayes 
