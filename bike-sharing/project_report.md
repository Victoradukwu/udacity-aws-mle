**Competition Report**

**The Best Performing Model**

The Autogluon TabularPredictor makes use of many models and uses the Ensemble technique to come up with the best result. In the first training round, no model was specified. Autogluon TabularPredictor used the default models:

'CatBoostModel', 'WeightedEnsembleModel', 'LGBModel', 'KNNModel', 'XTModel', 'XGBoostModel', 'RFModel', 'NNFastAiTabularModel'

Of all these WeightedEnsembleModel had the best performance, followed by XGBoostModel. This is shown in Fig1 of the attached file `support file.docx`.

In subsequent training rounds, custom values of hyperparameters were used to train XGBoost model. For each set of hyperparameters, predictions were generated and submitted to Kaggle. The results of this operation is tabulated in fig.2 of the attached file `support file.docx`


**Feature Engineering**

A bit of Feature Engineering was done to improve the perfoemance of the predictors.

This is the One-hot encoding of `season` feature.




**Hyperparameter Tuning**

A number of combinations of the hyperparameters were used. When the hyperparamters changed from the default, there was a clear increase in the Kaggle Score and the Model performance. However, with subsequent changes, there were noticeable changes in the model performance but the Kaggle submission score did not change. The default set of hyperparameters was not optimum.

This is shown in the attached file.

**Final Summary**

The first training run makes use of Autogluon TabularPredictor default models and hyperparameters. The ensemble technique was employed to get the final model. Among the base models, XGBBoost showed the best performance. Subsequent training round were done by combining different hyperparanters of the XGBoost Model and creating an EnsembleModel from it. The result shows an increase in performance and score for the second run. However, further changes in the hyperparamters, though adding marginal improvements, did not lead to corresponding increase in the Kaggle score.
