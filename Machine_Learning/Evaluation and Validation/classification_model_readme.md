# Classification Model Evaluation Metrics

Evaluation metrics are crucial for assessing the performance of classification models. This README provides detailed explanations and mathematical formulations for precision, recall, F1-score, and Receiver Operating Characteristic (ROC) curve.

## Precision, Recall, and F1-Score

Precision, recall, and F1-score are fundamental metrics for evaluating classification models, both for binary and multiclass classification tasks.

### Definitions:
- **Precision**: The proportion of true positive predictions among all positive predictions.
- **Recall** (Sensitivity or True Positive Rate): The proportion of true positive predictions among all actual positive instances.
- **F1-Score**: The harmonic mean of precision and recall, providing a balance between the two metrics.

### Mathematical Formulas:
- Let TP, TN, FP, and FN represent true positives, true negatives, false positives, and false negatives, respectively.

\[ \text{Precision} = \frac{TP}{TP + FP} \]

\[ \text{Recall} = \frac{TP}{TP + FN} \]

\[ \text{F1-Score} = \frac{2 \times \text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}} \]

## Receiver Operating Characteristic (ROC) Curve

The ROC curve is a graphical plot that illustrates the diagnostic ability of a binary classification model across various threshold settings.

### Definitions:
- **True Positive Rate (TPR)** (Recall or Sensitivity): The proportion of true positive predictions among all actual positive instances.
- **False Positive Rate (FPR)**: The proportion of false positive predictions among all actual negative instances.

### Mathematical Formulas:
\[ \text{TPR} = \frac{TP}{TP + FN} \]

\[ \text{FPR} = \frac{FP}{FP + TN} \]

## Example

Let's consider a binary classification model with the following confusion matrix:

|               | Predicted Negative | Predicted Positive |
|---------------|--------------------|--------------------|
| Actual Negative | 90 (TN)          | 10 (FP)           |
| Actual Positive | 5 (FN)           | 95 (TP)           |

Using the formulas above, we can calculate precision, recall, and F1-score. Additionally, we can plot the ROC curve using various threshold settings.

## Conclusion

Precision, recall, F1-score, and ROC curve are essential evaluation metrics for assessing the performance of classification models. By understanding these metrics and their mathematical formulations, practitioners can effectively evaluate and compare different classification models, gaining valuable insights into their predictive accuracy in real-world scenarios.