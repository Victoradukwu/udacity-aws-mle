**Competition Report**

**The Best Performing Model**

The Autogluon TabularPredictor makes use of many models and uses the Ensemble technique to come up with the best result. In the first training round, the data was used as-is and the default parameters of TabularPredictor was used. Autogluon TabularPredictor used these default models:

'CatBoostModel', 'WeightedEnsembleModel', 'LGBModel', 'KNNModel', 'XTModel', 'XGBoostModel', 'RFModel', 'NNFastAiTabularModel'

Of all these WeightedEnsembleModel had the best performance, followed by XGBoostModel.

**Feature Engineering**

In the second round of training the default TabularPredictor parameters were used. However, the data was pre-processed using a number of feature-engineering practices.
This is the One-hot encoding of `season` feature. Also the `weather` column was converted to categorical type using pandas `astype` function. In addition, the `datetime` column was decomposed into its constituent year, month, day.

This feature engineering led to a great improvement in the Kaggle score.


**Hyperparameter Tuning**

The main parameter that was tuned for TabularPredictor was the `presets`. Default value of `medium_quality_faster_train` was used for the first two rounds of training. For subsequent rounds, the values of `high_quality_fast_inference_only_refit` and `best_quality` were used. Each of these contributed to increase in the Kaggle score.

**Final Summary**

The first training run makes use of Autogluon TabularPredictor default models and hyperparameters. The ensemble technique was employed to get the final model. Among the base models, Ensemble showed the best performance, followed by XGBoost. Subsequent training round were done by using different values of TabularPredictor `presets`. The results show an increase in performance and score.
