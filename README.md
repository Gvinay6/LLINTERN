IMDb Movie Review Sentiment Analysis

This code performs sentiment analysis on movie reviews collected from the IMDb dataset. The sentiment analysis is carried out using a Support Vector Machine (SVM) classifier with a TfidfVectorizer for text feature extraction. Additionally, a grid search is employed to optimize hyperparameters for the SVM model.


Setup and Data Preparation

The code begins by importing necessary libraries such as NumPy, Pandas, Matplotlib, Seaborn, and scikit-learn. The IMDb dataset (IMDB Dataset.csv) is loaded into a Pandas DataFrame (df_review), containing reviews and corresponding sentiments. The dataset is then split into positive and negative sentiment subsets, each containing 5000 samples. Label encoding is performed on the sentiment labels for model training and evaluation. The dataset is further split into training and testing sets.


Model Training

The TfidfVectorizer is used to convert text data into numerical features. A pipeline is created with a dummy estimator as a placeholder, and a grid search is performed over hyperparameters for different SVM configurations. The best model is selected based on the grid search results.


Model Evaluation

The trained model is evaluated on the test set using metrics such as F1 score, accuracy, log loss, and ROC AUC score.


Save and Load Model

The best model is saved to a file using the joblib library. The saved model is loaded back into the script for further use.


IMDb Movie Reviews Web Scraping

The script includes a function (fetch_all_movie_names) that scrapes movie titles and links from an IMDb list. The user is prompted to input a movie name, and the corresponding IMDb URL and review link are displayed.

Movie Review Sentiment Analysis

For a selected movie, reviews are scraped using BeautifulSoup and requests. The scraped reviews are converted into a DataFrame with sentiment predictions. The popularity of the movie is determined based on the cumulative sentiment score over time.

Visualizations

Line plot depicting the popularity of the selected movie over time. Pie chart showing the distribution of sentiment predictions for the selected movie.
