# What are Regression Algorithms

* Regression Algorithms estimate things
* Each estimate in a regression alorithm is based on certain characteristics, for example:
  * A stock's current price
  * Target price
  * beta
  * industry

## How does the machine learning work with regression

* An algorithm is provided known data, characteristics, and known historical results.
* The model applies rules to the characteristics that will create the known outcome.
* The trained model is tested on a test set of data, then can be applied to data with an unknown outcome to predict the outcome.

### Vocabulary Terms

* Each 'thing' is an 'observation'
* Each 'estimate' is a 'prediction'
* Each 'characteristic' is a 'feature'
* Each 'rule' is a 'trained model'

## Real Relationships: Underfit, Good Fit, and Overfit

* **Underfit:** Real Relationship Complexity > Model Complexity
* **Good Fit:**  Real Relationship Complexity = Model Complexity
* **Overfit:** Real Relationship Complexity < Model Complexity
* **Error:** The variations that cannot be predicted by the model
  * It is possible to develop a model with little error, but **you cannot develop a model with zero error**.
  * Model Error is measured with the **R^2** (R-Squared) value, which is between 0 and 1.
  * If a model has an R^2 = 0.80, then that means 80% of variation in the target variable is explained by variation in the input variables.
  * This means the model has a good accuracy 80% of the time.
  * An overfit model red flag is producing an R^2 = 1.00.

### Desired Statistical Results

* Want a model that is generalizable, which means it performs equally well with trained data and unseen data.
* **Underfit:** R^2 with training data = **Low**, R^2 with new data = **Low**
* **Good Fit:** R^2 with training data = **High**, R^2 with new data = **High**
* **Overfit:** R^2 with training data = **High**, R^2 with new data = **Low**

## Preventing Overfitting with Regularization

* Too much data being used in the model can cause overfitting.
  * For example:  Target -> Predict someone's weight based on height.  
  * There is a correlation, but not the only correlation.   
  * Data may include: Weight, Height, Occupation, Sex.
  * These all would be good data to include in the model.
  * Data could also include: Hometown, Hour of Birth, and No. of hairs on head.
  * The model would create rules to fit this data if included, which would cause an overfit model, resulting in low accuracy with new data.
* **Regularization:** a form of automatic feature selection that dampens the effect of insignificant features, thus reducing overfitting
* **Cost Function:** The way you choose to quantify your model's error.
  * The most commonly used cost function is the **sum of squared errors**. 
  * To calculate the sum of squared errors:
    * Measure the error of each prediction
    * Square the error
    * Sum all the squared values
    * The result of this cost function is that extreme errors are more heavily penalized because their values are squared.
* Two types of penalties from the Cost Function
  * L1 penalizes the **absolute** size of model coefficients
  * L2 penalizes the **squared** size of model coefficients
* Three types of regularized linear regression algorithms to help minimize Cost Function:
  * **Lasso:** Regularized with the L1 penalty factor.
  * **Ridge:** Regularized with the L2 penalty factor.
  * **Elastic Net:** Regularized with the a blend of both penalty factors.
