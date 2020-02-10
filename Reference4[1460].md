### Detecting hospital-acquired infections: A document classification approach using support vector machines and gradient tree boosting

#### Summary

The team is trying to combat HAI by using various techniques. The paper revolves around the prediction of HAI from hospital records.

##### Techniques
###### SVM

It uses the concept of representing the documents that are to be classified as points in a high dimensional space and finding the hyperplane that separates them.

###### GTB

It utilizes the power of a forest of weak tree learners to approximate the sought-after classification function. By training a number of tree classifiers on different parts of the training data and then weighting their collective decision, a strong classifier is produced.

###### Term frequency(TF), Stop word removal,Infection-specific terms, Lemmatization and stemming

Trimming the document in order to make it more meaningful data set.  

##### Evaluvation

###### 10-fold cross-validation and Statistical tests

Cross-validation is especially useful if the dataset is small,such as in the team's case, as it maximizes the amount of training data. When comparing the classifiers results, statistical testing is necessary in order to verify the significance of the results.

##### Results

The team achieved an average of 70-75 percent precision using all these techniques.

##### Authors

Claudia Ehrentraut, Markus Ekholm, Hideyuki Tanushi, Jörg Tiedemann, Hercules Dalianis
