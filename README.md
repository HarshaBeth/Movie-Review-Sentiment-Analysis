# Movie Reviews Sentiment Analysis (NLP)
I have built this sentiment analysis project for my Natural Language Processing module at the British University in Dubai. This project aims to help businesses, like Netflix and Amazon Prime,
grow their profits by understanding which movies are given negative reviews and which have positive reviews. They can do so by putting the positive reviewed movies at the top of 
the "suggested" list.
***
<ins>First step</ins>

I gathered a movie reviews dataset with 50,000 reviews having equal amounts of positive and negative reviews. Furthermore, I pre-processed the data by removing strings that 
would cause parsing errors (such as quotations and HTML tags) and also removing stopwords. In the next pre-processing step, I separated the positive and negative reviews into their separate lists. 
Then I made the two lists into two big strings joining all the elements together. We do so to be able to tokenize and normalize our data. 

Second step) after some research I decided to utilize the TweetTokenizer for tokenization as its main purpose is to tokenize informal phrases and symbols such as those used in our 
movie reviews dataset. For visualisation I used the frequency distribution function from the nltk library to see what words have higher frequencies in their sentiment group. This way I 
am able to know the correlation between certain words and their respective groups. Moving forward, I extracted the features from both positive and negative strings and labeled them as positive
or negative. 

Third step) I combined all these labeled words into one big string to split this data into training and testing data with an 8:2 split. The classifier I used was the Naive Bayes Classifier
because of its speed and efficiency. However, I did get an accuracy of 60% for our model, but this is due to not having a larger dataset with more accurate inputs. After all these steps,
I simply created a GUI using Tkinter library, where the user can write their movie review and our model will predict whether the user is happy or dissatisfied with the movie.

Extra step) I integrated OpenAI to further enhance our predictions by giving our results a rating from 1 to 5 (1 being very negative and 5 being very positive). This way it is possible to see
the "level" of the review as well as the sentiment to a certain movie.
