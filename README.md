# LyricsMood
## A machine learning approach to classify songs' lyrics by mood

The goal of this project is to build a recommendation system for users who wants to listen to happy or sad songs. LyricsMood is able to predict whether a song is happy or sad based on its lyrics.

### Links
* [Demo Application](http://francescocucari.pythonanywhere.com/)
* [Data collection (IPython Notebook)](https://github.com/kuka93/lyricsmood/blob/master/code/collect_data.ipynb)
* [Model training using binary features (IPython Notebook)](https://github.com/kuka93/lyricsmood/blob/master/code/model_training_1.ipynb)
* [Model training using TFIDF (IPython Notebook)](https://github.com/kuka93/lyricsmood/blob/master/code/model_training_2.ipynb)
* [Technical report](http://www.slideshare.net/FrancescoCucari/mood-classification-of-songs-based-on-lyrics)

### Summary
* __Dataset overview__

The *happy* and *sad* song details (title and artist) are collected by crawling last.fm. Song details are used to get the proper URL to get the lyrics that are collected by crawling metrolyrics.com. All songs for which lyrics have not been available were removed from the dataset. Furthermore, non-english songs are removed from the dataset.
The dataset contains 3.332 songs (1.499 happy songs and 1.904 sad songs).

* __Exploratory data analysis__

wordcloud *Happy*:

![wordcloud Happy](https://github.com/kuka93/lyricsmood/blob/master/images/wordcloud_happy.jpg)

wordcloud *Sad*:

![wordcloud Sad](https://github.com/kuka93/lyricsmood/blob/master/images/wordcloud_sad.jpg)

* __Results__

![results](https://github.com/kuka93/lyricsmood/blob/master/images/results.jpg)

__Model performance of the song lyrics classifier.__ A: Receiver operating characteristic (ROC) curves of the Bernoulli naive Bayes classifier performance using a 2-gram sequence model tfidf as feature vectors for song lyrics classification by mood. The performance was evaluated via 10-fold cross validation on the lyrics dataset. The true positive rate was calculated from songs labeled as happy that were correctly classified, and the false positive rate was calculated from sad songs that were misclassified as happy. B is the confusion matrix of the classifier based on a testing dataset.

__The accuracy is: 0,87 +/- 0,06.__ The performance was evaluated via 10-fold cross validation on the lyrics dataset. Further results can be found in the technical report
