# Converseon

### How to run this program
There are four parts in this program.
1. Use the function 'load_data' to read and transform the json training data to a pandas data frame. This function returns a data frame contains features information (train_X) and a series contains target information (train_y).
2. By setting the path to the place holds training data and calling the function 'load_data', create train_X and train_y for model building.
3. The class 'FlowerTrainer' is used to train the model, and it contains three methods: train, evaluate, and save. Inside of the train method, a KNN (k=3) model is built based on the training data. Inside of the evaluate mehtod, the KNN model is evaluated by apply cross validation with 10 folds. Inside of save method, the KNN model is saved to a local file.sdf
4. The class 'FlowerClassifier' is used to predict/classify the test data, contains two methods: load and predict. Inside of load method, the KNN model is loaded. Inside of predict method, the test data is loaded from json and transformed to a pandas data frame. Moreover, the predicted labels based on test data are saved to a json file.

In order to run this program, please call the function 'load_data', class 'FlowerTrainer', and class 'FlowerClassifier'.
The KNN model has a prediction accuracy rate at 0.967 by averaging scores from a cross validation with 10 folds.
### Bonus Question
1. Is it possible to use Logistic Regression to do multi-class classification? If yes, can you implement Logistic Regression method in your train function?
* Answer: Yes, it is possible to use Logistic Regression to do multi-class classification. 

2. If you were to evaluate your classifier, explain in one paragraph that what kind of metrics you could have provide and/or how you would have separate your test from training data.
* Answer: I used the metric accuracy to evaluate my KNN classifier. I also applied a 10 fold cross validation to minimize the randomness caused by data set splitting.
