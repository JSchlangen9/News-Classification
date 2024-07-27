# DTSA 5510: News Classification Project

## Project Overview

For this project, I will be analyzing the BBC News Classification Dataset using matrix factorization techniques. The dataset includes text of various news articles that are broken out into 5 different categories (Sports, Politics, Business, Entertainment, & Tech). The model will aim to classify the news article into the correct category.

## Exploratory Data Analysis

There is not much to be done in terms of data cleaning, so we can move directly into exploratory data analysis. I created 3 visualizations that were of interest to me relating to the data set. The first was a simple histogram showing the category of article and the number of those articles in the dataset. I wanted to get a feel for the represenetation of each article type, and as shown, we have a similar number of each article type in the dataset. Secondly, I thought it would be interesting to see a distribiution of the length of each article. We can see that the length of article is roughly normally distributed with a long tail in the positive direction. We also see a median article length of roughly 2,000 characters. Lastly, I wanted to explore the most common word in each of the articles. It was not surprising to see that the most common words were: to, the, in, & of. In a future iteration of this project, I would prefer to exclude common words in the english language and try this type of analysis again.

## Unsupervised Model

In the unsupervised model, I translated each article text into a vector using python's Word2Vec library. From here, I was able to use Sklearn's Non-Negative Matrix Factorization model to derive predictions for the dataset. Unfortunately, I got a very low accuracy score of only 19%, and I believe that this is due to errors relating to the use of python's Word2Vec library.

## Supervised Model

In the supervised model, I decided to use sklearn's Random Forest Classifier, as this is a model that I am most comfortable with. I again translated each article text into a vector using python's Word2Vec library. With the vectors, I was able to feed them into the Random Forrest model and derive predictions with them. Again, I got a very low accuracy score of only 30%, however this was significantly better than the unsupervised model. I still believe that the low accuracy is directly related to the usage of python's Word2Vec library.

## Results & Conclusion

I found that the supervised model works significantly better than an unsupervised model in this scenario. This is because we have the category labels included in the dataset, so this makes it much easier for the model to learn from. My initial conclusion is to only use unsupervised models when absolutely necessary, and in the event that we cannot build a supervised model.
