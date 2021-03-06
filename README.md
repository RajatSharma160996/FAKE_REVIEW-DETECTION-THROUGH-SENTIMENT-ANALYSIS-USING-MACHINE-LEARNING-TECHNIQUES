# FAKE_REVIEW-DETECTION-THROUGH-SENTIMENT-ANALYSIS-USING-MACHINE-LEARNING-TECHNIQUES
DATA MINING PROJECT

This project is a part of My Course Work , under the subject DATA MINING.		
This project aims of Detection of fake review using sentimental analysis using machine learning algorithm, for this I have implemented 

Step-By-Step Explanation of Detection of Fake Review.
1. Load the Dataset.
2. Shuffle the Dataset.
3. Changed the Label from __label1__ to FAKE and __label2__ to REAL.
4. Splitting Dataset for Training and Testing.

# First algorithm is Naive Bayes
Naive Bayes Classifier from scratch,for prediction of label to review.
Naive Bayes is a Supervised Machine Learning Algorithm so it takes set of pre labeled data as input for training purpose and after training it predicts label for new unlabeled test input based on training.

This part mainly contain functions which are as mention:

preprocess() for text preprocessing which include extracting important features , tokenization, lemmetization and bigram creation then it append the new text into one list which is  used as input.
split() for spliting whole dataset into training and test set.
trainclassifier() for training of classifier
predict() for prediction of labels to new unlabeled data
crossvalidation() for 10 fold cross validation for improving accuracy of classifier

At the end I have created Accuracy(), Precision() , Recall() and F1_score() functions for calculation of evaluation parameter


# Second algorithm is SVM

A SVM model is used that classifies the reviews as REAL or FAKE. Used both the review text and the additional features contained in the data set to build a model that predicted with over 80% accuracy.

Training the Model using Train Dataset:
1. Parsing the datas from the Train set which are required.
2. Pre-processing the Text Data in the Train set by removing Stop-words and punctuations and Lemmatizing the tokens. 
3. Calculating TF-IDF for each document available in the Train Set. For Calculation of TF-IDF value:
  a. Calculate TF (Term Frequency) of each document. Which is counting of each token appears how many times in that document divides to the      length of the document and maintain a global dictionary of all the token which appears in all the documents with there counts.
  b. Calculate IDF (Inverse Document Frequency) which is calculated using the whole training set document count and the global dictionary.
     IDF = log( Total Number of documnents / occurrences of that term in all the documents )
  c. Calculate TF-IDF which is multiply both TF and IDF term for the document.
4. This TF-IDF output is used as input for the Linear SVM classifier. 
   (Here, Label is also added as for training we require both Data and corresponding Label)
   
Testing the Model using Test Dataset:
1. Do all the parsing and pre-procesiing for the Test set which is done for the training set as well.
2. Compute the TF-IDF values for the Test set.
3. Now, predict the labels for documents of Test set.
4. Evaluate the difference between the true label and the predicted labels.

Used Accuracy, Precision, Recall and F1-Score as the evaluation metrics for the model.

Cross-Validation is used to improve the accuracy of the Model. Here, folds is taken as 10.

Same approach is used for Bigram tokenization of the text. Above is done for unigram model.

Also, Term Occurences is used rather than TF-IDF computation. With both Unigram and Bigram model. 

Files contained in the folder FAKE_REVIEW_DETECTION_THROUGH_SENTIMENT_ANALYSIS_USING_MACHINE_LEARNING_TECHNIQUES :

TF_IDF_SVM : Contains the code of TF-IDF with SVM classifier. (Used both the review text and the additional features contained in the                 data set )

TF_IDF_SVM_WITH_BIGRAM : Contains the code of TF-IDF with SVM classifier with Bigram tokens as input. (Used both the review text and the                          additional features contained in the data set )

TO_SVM : Contains the code of Term occurrences with SVM classifier.

TO_SVM_BIGRAM : Contains the code of Term occurrences with SVM classifier with Bigram tokens as input.

