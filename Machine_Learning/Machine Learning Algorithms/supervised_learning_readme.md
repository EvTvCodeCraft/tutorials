# Supervised Learning Algorithms

Supervised learning algorithms are essential tools in predictive modeling tasks, where the goal is to learn patterns from labeled data. This README provides comprehensive explanations, methodologies, and mathematical formulations for popular supervised learning algorithms.

## Linear Regression

Linear Regression is a straightforward and widely used algorithm for modeling the relationship between a dependent variable and one or more independent variables.

### Methodology:
1. **Model Representation**: 
   - The linear regression model is represented as \( \hat{y} = \theta_0 + \theta_1 x_1 + \theta_2 x_2 + \ldots + \theta_n x_n \), where \( \hat{y} \) is the predicted value, \( x_i \) are the input features, and \( \theta_i \) are the model parameters (coefficients).

2. **Objective Function (Cost Function)**:
   - The objective is to minimize the mean squared error (MSE) between the predicted and actual values:
     \[ J(\theta) = \frac{1}{2m} \sum_{i=1}^{m} (\hat{y}^{(i)} - y^{(i)})^2 \]
   - Where \( m \) is the number of training examples, \( \hat{y}^{(i)} \) is the predicted value for the \( i^{th} \) example, and \( y^{(i)} \) is the actual value.

3. **Parameter Estimation**:
   - Parameters \( \theta \) are estimated using optimization algorithms like Gradient Descent, minimizing the cost function \( J(\theta) \).

### Applications:
- Predicting house prices, stock prices, etc.

## Logistic Regression

Logistic Regression is a binary classification algorithm that models the probability of a binary outcome based on one or more independent variables.

### Methodology:
1. **Model Representation**:
   - The logistic regression model transforms the output of a linear regression model using the logistic (sigmoid) function:
     \[ h_{\theta}(x) = \frac{1}{1 + e^{-\theta^T x}} \]

2. **Objective Function (Cost Function)**:
   - The objective is to maximize the likelihood of the observed data, leading to the cross-entropy loss function:
     \[ J(\theta) = -\frac{1}{m} \sum_{i=1}^{m} [y^{(i)} \log(h_{\theta}(x^{(i)})) + (1 - y^{(i)}) \log(1 - h_{\theta}(x^{(i)}))] \]

3. **Parameter Estimation**:
   - Parameters \( \theta \) are estimated using optimization algorithms like Gradient Descent, minimizing the cost function \( J(\theta) \).

### Applications:
- Email spam detection, disease diagnosis, etc.

## Decision Trees

Decision Trees are versatile algorithms that recursively partition the feature space into regions based on simple decision rules.

### Methodology:
1. **Splitting Criterion**:
   - Decision tree nodes are split using various criteria such as Gini impurity or information gain.

2. **Decision Rule**:
   - At each node, the decision rule is based on a feature and threshold, resulting in binary splits.

3. **Stopping Criteria**:
   - Recursive splitting stops based on criteria like maximum depth, minimum samples per leaf, or purity thresholds.

### Applications:
- Classification and regression tasks in various domains.

## Support Vector Machines (SVM)

Support Vector Machines are powerful algorithms for both classification and regression tasks, finding the optimal hyperplane that separates the classes or predicts continuous outcomes.

### Methodology:
1. **Optimization Problem**:
   - SVM seeks to find the maximum-margin hyperplane that separates the classes:
     \[ \min_{\theta, b} \frac{1}{2} ||\theta||^2 \]
     subject to \( y^{(i)}(\theta^T x^{(i)} + b) \geq 1 \) for all training examples.

2. **Kernel Trick**:
   - SVM can efficiently handle non-linear classification tasks by mapping input data into higher-dimensional feature spaces using kernel functions.

### Applications:
- Image classification, text classification, etc.

## k-Nearest Neighbors (k-NN)

k-Nearest Neighbors is an intuitive algorithm that makes predictions based on the majority class of its nearest neighbors in the feature space.

### Methodology:
1. **Distance Metric**:
   - Common distance metrics include Euclidean distance, Manhattan distance, or Minkowski distance.

2. **Voting Mechanism**:
   - The majority class among the \( k \) nearest neighbors determines the class label of the query instance.

### Applications:
- Recommendation systems, pattern recognition, etc.

## Naive Bayes

Naive Bayes is a probabilistic classifier based on Bayes' theorem with the assumption of independence between features.

### Method

ology:
1. **Conditional Probability**:
   - Naive Bayes calculates the conditional probability of each class given the features:
     \[ P(y | x_1, x_2, \ldots, x_n) = \frac{P(y) \times P(x_1 | y) \times P(x_2 | y) \times \ldots \times P(x_n | y)}{P(x_1) \times P(x_2) \times \ldots \times P(x_n)} \]

2. **Model Training**:
   - Naive Bayes estimates probabilities from training data and selects the class with the highest posterior probability as the prediction.

### Applications:
- Text classification, spam filtering, etc.

## Conclusion

Supervised learning algorithms are essential components of predictive modeling tasks. By understanding the methodologies, mathematical formulations, and applications of Linear Regression, Logistic Regression, Decision Trees, Support Vector Machines, k-Nearest Neighbors, and Naive Bayes, practitioners can effectively choose and apply the most suitable algorithm for their specific problem domain.