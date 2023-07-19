# Using ML for predict Miles in Uber
#### made by [@pelmeshek1706](https://telegram.me/pelmeshek1706)

### In this project, I have been predicting the number of miles based on features such as
- Trip Category,
- Start and End Points,
- and trip start parameters such as "Hour", "Month" and "Day оf week" of Trip.

After the EDA, it was found that business trips are favored as long trips and personal trips for small ones are favored as city or regional trips.

Classical variants of machine learning were used as predictive models. Their results (without additional parameters) are presented in the table below :

|№|	Model|	MSE|	MAE|	R-squared|
|-|------|-----|-------|-------------|
|0|	Linear Regression|	342.385935|	6.602412 |	0.516833|
|1|	Decision Tree	|213.063636	|5.445022 |0.699329 |
|2|	Random Forest	|81.991518	|3.795094 |	0.884295 |
|3|	SVR	|658.539953	|6.882846|	0.070683|
|4|	XGBoost	|82.968912 |	3.751851 |	0.882916|
|5|LightGBM	|162.366676	|4.673704 |	0.770872|
|6|	Gradient Boosting Regressor	|88.441363	|4.026233| 0.875194|
|7|	ADA Boost	|144.220526|9.166122	|0.796479|
|8|	Linear SVR	|322.898470	|5.311749	|0.544333|

### Since the reference value for MAE and MSE metrics is 0 and for R-squared is 1, RandomForest wins on these metrics

Since the training used simple models with no special parameters, I used GridSearch to improve the results.
Best parameters selected by GridSearch:
- max_depth: None
- min_samples_split: 2
- n_estimators: 100


Data that I used - [Uber Dataset](https://www.kaggle.com/datasets/bhanupratapbiswas/uber-data-analysis)

