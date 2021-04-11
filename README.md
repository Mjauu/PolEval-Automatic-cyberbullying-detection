# PolEval-Automatic-cyberbullying-detection
http://poleval.pl/tasks/task6

Binary classification problem
- normal/non-harmful tweets (class: 0)
- tweets that contain any kind of harmful information (class: 1)

Method 1:
- TF-IDF Vectorizer + ngrams (2-1) on lemma, all lowercase, only digits and letters, no html tags and urls, no stopwords, 4 most common words excluded

Method 2:
- Preprocessing by removing emoji and @anonymous token or replace emoji by character set e.g. :) and replace @anonymouse with @osoba.
- Bert model (dkleczek) to extract classification vector for given twitt (average pooling over the word tokens), no fine-tuning, then evaluate vector on logistic regression, SVM, random forest, KNN, Bayes.
- Additionally, there is a small playground, where I do cosine similarity between feature vectors e.g. harmful vs non-harmful, the basic correlation between elements in the f. vec, dimensionality reduction, and plotting
