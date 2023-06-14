# mini-project-V

## Project Goals
To explore NLP by seeing if a simple TF-IDF and logistic regression model can detect duplicate Quora questions.

### Data

The labeled dataset can be downloaded from [here](https://drive.google.com/file/d/19iWVGLBi7edqybybam56bt2Zy7vpf1Xc/view?usp=sharing).

As there is no test set, I started with a train-test split before jumping into the data to simulate a real world situation.

## EDA

Discovered that the repeated appearances of questions in the dataset followed some sort of log relationship, where the vast majority of questions appeared only once in the dataset. About 63% of the entries were flagged as non-duplicates.

## Process

### Data Cleaning

Null question values were imputed with an empty string. 

### Natural Language Preprocessing

Followed standard steps of removing punctuation, setting characters to lowercase, removing stop words, and performing stemming.

### Feature Engineering

Trained a TF-IDF vectorizer on both question columns within the training data. This was then used to vectorize both the training and test data into a final form to be used in a model.

### Logistic Regression

Class balancing was performed just before performing grid search to tune for hyperparameters. Then the model was retrained with the best found parameters, and predictions were made on the test set.

## Results

The results were dissapointing, with an accuracy of 62.5% which was below baseline.

## Challenges

Limited time and energy were the main barriers on this project, and so the scope was dramatically reduced.

## Future Goals

I would love to try other classification models and do more feature engineering, specifically Google's word2vec model.