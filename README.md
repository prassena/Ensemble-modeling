# Ensemble-modeling
Ensemble modeling applied on DonorsChoose Dataset

What is Ensembling mean here in Machine Learning?
Ensemble modeling is the process of running two or more related but different analytical models and then synthesizing the results into a single score or spread in order to improve the accuracy of predictive analytics.

There are lot of Ensemble models some of the widely used and popular Ensemble model are Bagging,Boosting,Stacking and Cascading

# Bagging:
One of the Bagging model is Random Forest.
we find lot of trees in forest ,same way here we build lot of decission trees (base learners)and the data we used to build the base learners is selected randomly (row sampling and column sampling) .so that all the tree will be different.

The trees we build will be of high variance and low biased but the final model which is like a majority voting type of model will be of less variance and less biased.

# Boosting:
One of the Boosting algorithm is Gradient Boosted Decision Trees.
In this techinique we build our base learnes with high biase and low variance .The model we build will learn from previous models error.we can reduce any kind of loss even when we build a decission tree model ,as we use pseudo-residuals(negative derivative of given loss function) to build models.

Boosting is mostly used to reduce the bias in a model.

# Stacking:
we build lot of perfect models using different algorithm like logical regression,SVM,Decission Tree and build a meta classifier on top of it, which uses the output of all the models built as input and predict the output.

Stacking is mostly used to increase the prediction accuracy of a model. For implementing stacking we will use the mlextend library provided by sci-kit learn

# Cascading:
We build a model which is 100 percent sure about the prediction,if the predicted probablity is less than 100% then the data point is sent to more complex model which was trained on failure cases of orginal data point.

This class of models are very very accurate. Cascading is mostly used in scenarios where you cannot afford to make a mistake. For example, a cascading technique is mostly used to detect fraudulent credit card transactions, or maybe when you want to be absolutely sure that you don’t have cancer.
