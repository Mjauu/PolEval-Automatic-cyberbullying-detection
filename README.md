# PolEval-Automatic-cyberbullying-detection
http://poleval.pl/tasks/task6

Binary classification problem
- normal/non-harmful tweets (class: 0)
- tweets that contain any kind of harmful information (class: 1)

Method 1:
- TF-IDF Vectorizer + ngrams (2-1) on lemma, all lowercase, only digits and letters, no html tags and urls, no stopwords, 4 most common words excluded

![obraz](https://user-images.githubusercontent.com/56317534/114300949-d0a8fa00-9ac2-11eb-8602-2fb9f4fe91d8.png)


Method 2:
- Preprocessing by removing emoji and @anonymous token or replace emoji by character set e.g. :) and replace @anonymouse with @osoba.
- Bert model (dkleczek) to extract classification vector for given twitt (average pooling over the word tokens), no fine-tuning, then evaluate vector on logistic regression, SVM, random forest, KNN, Bayes.
- Additionally, there is a small playground, where I do cosine similarity between feature vectors e.g. harmful vs non-harmful, the basic correlation between elements in the f. vec, dimensionality reduction, and plotting

![obraz](https://user-images.githubusercontent.com/56317534/114300946-cb4baf80-9ac2-11eb-8735-846c03f833a2.png)
