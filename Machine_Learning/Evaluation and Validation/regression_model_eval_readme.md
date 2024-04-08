# Regression Model Evaluation Metrics

Evaluation metrics are crucial for assessing the performance of regression models. This README provides detailed explanations and mathematical formulations for Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared.

## Mean Absolute Error (MAE)

Mean Absolute Error (MAE) measures the average absolute difference between the predicted values and the actual values.

### Mathematical Formula:
\[ \text{MAE} = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i| \]

Where:
- \( n \) is the number of samples.
- \( y_i \) is the actual value.
- \( \hat{y}_i \) is the predicted value.

## Mean Squared Error (MSE)

Mean Squared Error (MSE) measures the average of the squares of the errors between the predicted values and the actual values.

### Mathematical Formula:
\[ \text{MSE} = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2 \]

## R-squared (Coefficient of Determination)

R-squared (R2) represents the proportion of the variance in the dependent variable that is predictable from the independent variables.

### Mathematical Formula:
\[ R^2 = 1 - \frac{\sum_{i=1}^{n} (y_i - \hat{y}_i)^2}{\sum_{i=1}^{n} (y_i - \bar{y})^2} \]

Where:
- \( \bar{y} \) is the mean of the actual values.

## Example Calculation

Let's consider a regression model with the following predicted and actual values:

| Actual (y) | Predicted (\( \hat{y} \)) |
|------------|---------------------------|
| 10         | 12                        |
| 20         | 18                        |
| 30         | 28                        |
| 40         | 35                        |
| 50         | 48                        |

### MAE Calculation:
\[ \text{MAE} = \frac{|10 - 12| + |20 - 18| + |30 - 28| + |40 - 35| + |50 - 48|}{5} \]
\[ = \frac{2 + 2 + 2 + 5 + 2}{5} \]
\[ = \frac{13}{5} \]
\[ = 2.6 \]

### MSE Calculation:
\[ \text{MSE} = \frac{(10 - 12)^2 + (20 - 18)^2 + (30 - 28)^2 + (40 - 35)^2 + (50 - 48)^2}{5} \]
\[ = \frac{4 + 4 + 4 + 25 + 4}{5} \]
\[ = \frac{41}{5} \]
\[ = 8.2 \]

### R-squared Calculation:
\[ \bar{y} = \frac{10 + 20 + 30 + 40 + 50}{5} = \frac{150}{5} = 30 \]
\[ \text{Total Sum of Squares (TSS)} = \sum_{i=1}^{5} (y_i - \bar{y})^2 = (10 - 30)^2 + (20 - 30)^2 + (30 - 30)^2 + (40 - 30)^2 + (50 - 30)^2 = 800 \]
\[ \text{Residual Sum of Squares (RSS)} = \sum_{i=1}^{5} (y_i - \hat{y}_i)^2 = (10 - 12)^2 + (20 - 18)^2 + (30 - 28)^2 + (40 - 35)^2 + (50 - 48)^2 = 41 \]
\[ R^2 = 1 - \frac{RSS}{TSS} = 1 - \frac{41}{800} \approx 0.9488 \]

## Conclusion

Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared are crucial evaluation metrics for assessing the performance of regression models. By understanding these metrics and their mathematical formulations, practitioners can effectively evaluate and compare different regression models, gaining valuable insights into their predictive accuracy in real-world scenarios.