# should-we-watch-this
Objective: Predicting if a movie is worth your time by using NLP to create a Sentiment Classifier that analyzes movie reviews and returns a pos/neg Sentiment Label. Data from the Stanford AI Lab's Large Movie Review Dataset (https://ai.stanford.edu/~amaas/data/sentiment/) was used for this project.

Business Understanding: IMDB allows users to write reviews for movies and provide a rating on a scale from 1-10. These reviews and ratings can be used to judge the quality of a movie the user has not seen and can be used as a building block towards quantifying user preferences and building a content recommender.

Data Understanding: The dataset contains 50k movie reviews evenly split into balanced testing and training sets. There are no more than 30 reviews for any given movie and all neutral reviews (4-6 out of 10) have been removed. Positive (pos) reviews are all >= 7 and Negative (neg) reviews are <= 4. Additionally, there are binary sentiment polarity labels attached to each review. 1 is pos, 0 is neg.

Data Preparation: Cleaned and processed text training dataset to create word tokens and a Bag of Words(BoW) by removing stopwords, punctuation, stemming and lemmatizing. From there, the BoW was vectorized using the TF-IDF formula and then split into Train/Test using an 80/20 breakdown.

Modeling: Two models were used for this project, a Logistic Regression Model and a Random Forest model. Both models were trained with an 80/20 Train/Test split from the training data and used the default model parameters to establish a baseline for performance improvement.

Evaluation: The performance of these models was evaluated using the precision and accuracy scores and visualized using a Confusion Matrix and an ROC Curve

Deployment: After tuning the models using the Training data, the models were applied to the 25k Testing reviews. These reviews were also balanced (12.5k neg and 12.5k pos) and omitted any neutral reviews.