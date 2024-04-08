# Evaluation Metrics in Machine Learning

Evaluation metrics are essential for assessing the performance of machine learning models. This README explores various evaluation metrics in detail, including accuracy, precision, recall, F1-score, confusion matrix, ROC curves, and AUC.

## Accuracy, Precision, Recall, and F1-Score

Accuracy, precision, recall, and F1-score are fundamental metrics for evaluating classification models.

### Definitions:
- **True Positives (TP)**: Instances correctly predicted as positive.
- **True Negatives (TN)**: Instances correctly predicted as negative.
- **False Positives (FP)**: Instances incorrectly predicted as positive (Type I error).
- **False Negatives (FN)**: Instances incorrectly predicted as negative (Type II error).

### Mathematical Formulas:
- **Accuracy**: 
\[ \text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN} \]

- **Precision**: 
\[ \text{Precision} = \frac{TP}{TP + FP} \]

- **Recall** (Sensitivity or True Positive Rate):
\[ \text{Recall} = \frac{TP}{TP + FN} \]

- **F1-Score**: 
\[ \text{F1-Score} = \frac{2 \times \text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}} \]

## Confusion Matrix

A confusion matrix provides a tabular representation of the model's predictions compared to the actual labels.

### Definitions:
- **True Positive Rate (TPR)** (Recall or Sensitivity): 
\[ \text{TPR} = \frac{TP}{TP + FN} \]

- **False Positive Rate (FPR)**: 
\[ \text{FPR} = \frac{FP}{FP + TN} \]

## ROC Curves and AUC

Receiver Operating Characteristic (ROC) curves and Area Under the Curve (AUC) are useful for evaluating binary classification models across different threshold settings.

### Definitions:
- **ROC Curve**: 
\[ \text{TPR} = \frac{TP}{TP + FN} \]
\[ \text{FPR} = \frac{FP}{FP + TN} \]

- **AUC**: The area under the ROC curve, providing a single scalar value representing the model's performance.

## Example

Let's consider a binary classification problem with the following confusion matrix:

|               | Predicted Negative | Predicted Positive |
|---------------|--------------------|--------------------|
| Actual Negative | 90 (TN)          | 10 (FP)           |
| Actual Positive | 5 (FN)           | 95 (TP)           |

From this confusion matrix, we can calculate various metrics:

- Accuracy: \( \text{Accuracy} = \frac{90 + 95}{90 + 10 + 5 + 95} = \frac{185}{200} = 0.925 \)
- Precision: \( \text{Precision} = \frac{95}{95 + 10} = \frac{95}{105} \approx 0.905 \)
- Recall: \( \text{Recall} = \frac{95}{95 + 5} = \frac{95}{100} = 0.95 \)
- F1-Score: \( \text{F1-Score} = \frac{2 \times 0.905 \times 0.95}{0.905 + 0.95} \)

## Conclusion

Evaluation metrics such as accuracy, precision, recall, F1-score, confusion matrix, ROC curves, and AUC are essential for assessing the performance of machine learning models comprehensively. By understanding these metrics and their mathematical formulations, practitioners can effectively evaluate and compare different models, gaining valuable insights into their performance in real-world scenarios.