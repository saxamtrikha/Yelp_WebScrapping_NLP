# Yelp Reviews Sentiment Analysis

The project is performed for sentiment analysis using Naive Bayes classifier by scraping over 5000+ reviews and star ratings of Toronto restaurants with Yelp Fusion API.
Reviews and star ratings of various Toronto restaurants is used as training data for the Naive Bayes classifier to do sentiment analysis into positive and negative classes.

Web Scraping
Scraped reviews and star ratings content from business URLs obtained from the Yelp Fusion's business API. Once the URLs are obtained, iterate through all the restaurants' response objects to fetch reviews and star ratings. The limit of 50 restaurants and 100 reviews per restaurant is kept to prevent overloading of public website. A total of 5000 reviews has been fetched.

Data preparation
Once the reviews are fetched, the data is split into positive and negative reviews based on user's star ratings. If star rating is > 3 then review is tagged positive, otherwise it is tagged negative. Fetched data had 4205 positive reviews and just 795 negative reviews. In order to address imbalance of the dataset, oversampling of negative reviews is done. Due to oversampling of negative reviews, the review count increases to 8410.

Naive Bayes Classifier
Data is now split into training and validation dataset. Using Sentiment Analyzer, naive bayes classifier is trainied. This trained model is used on validation dataset set aside from the training data which gave an accuracy of 78.87% with an F-measure [negative]: 76.81268882175226 and F-measure [positive]: 80.59418457648546. Improvements can be made on the model by fetching more data.
