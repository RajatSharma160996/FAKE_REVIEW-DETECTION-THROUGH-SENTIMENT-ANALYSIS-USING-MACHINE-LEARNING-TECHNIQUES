# FAKE_REVIEW-DETECTION-THROUGH-SENTIMENT-ANALYSIS-USING-MACHINE-LEARNING-TECHNIQUES
DATA MINING PROJECT

This project is a part of My Course Work , under the subject DATA MINING.		
This project aims of Detection of fake review using sentimental analysis using machine learning algorithm, for this I have implemented Naive Bayes Classifier from scratch,for prediction of label to review.
Naive Bayes is a Supervised Machine Learning Algorithm so it takes set of pre labeled data as input for training purpose and after training it predicts label for new unlabeled test input based on training.
This project mainly contain functions which are as mention:
preprocess() for text preprocessing which include extracting important features , tokenization, lemmetization and bigram creation then it append the new text into one list which is  used as input.
split() for spliting whole dataset into training and test set.
trainclassifier() for training of classifier
predict() for prediction of labels to new unlabeled data
crossvalidation() for 10 fold cross validation for improving accuracy of classifier

At the end I have created Accuracy(), Precision() , Recall() and F1_score() functions for calculation of evaluation parameter


