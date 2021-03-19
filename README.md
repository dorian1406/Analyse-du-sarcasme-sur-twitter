# Analyse-du-sarcasme-sur-twitter

After having received the various preprocessed data, it is a question of choosing an adequate classifier which will allow us to work better on our data. The ap- proach used was inspired by the work of Kreuz and Caucci. The data collection was based on different hashtag while keeping much more messages expressing sarcasm. In addition, we were also interested in lexical and pragmatic functions, however, by combining punctuations and interjections, responses to tweets.


1.1 Features selected for our classifier
In order to use a linear classifier, we had to select a few features. The image below shows the different features used for the proper functioning of our model. Among these we can mention stopwords (which allowed us to delete certain words which we would not like to take up space in the database), tweetTok- enizer (which is a lexical analyzer) and many others.


With the data base received, two essential things interested us in particular the tweetclean and the label (which are worth 0 or 1 depending on the presence or no negative words) as the following pseudo table shows us.


1.2 SVM classifier
The goal for an SVM model is to learn how to draw the line between two categories.Looking at the table in Figure 2, we see that we had to work more than 31961 tweets. In our case we have divided the data into a set of training (train) and test. We only take tweets with which we are very confident (stopword allows us to do good filtering and ngrams allows us to separate the different words).
We use the library BeautifulSoup to process the html encoding present in some tweets due to scrapping.
The function grid-Svm.fit was very useful to us because it allowed us to find the best combinations between the parameters passed to it. So we could have thanks to grid-svm-score the score obtained from our model as shown in the following figure.




