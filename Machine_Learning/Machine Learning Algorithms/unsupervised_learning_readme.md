# Unsupervised Learning Algorithms

Unsupervised learning algorithms are invaluable tools for exploring and discovering patterns within unlabeled data. This README provides comprehensive explanations, methodologies, and mathematical formulations for popular unsupervised learning algorithms.

## K-Means Clustering

K-Means Clustering is a simple yet powerful algorithm for partitioning data into K distinct clusters.

### Methodology:
1. **Initialization**:
   - Randomly initialize K cluster centroids: \( \mu_1, \mu_2, \ldots, \mu_K \).

2. **Cluster Assignment**:
   - Assign each data point \( x^{(i)} \) to the nearest cluster centroid \( \mu_j \):
     \[ \text{min}_j ||x^{(i)} - \mu_j||^2 \]

3. **Centroid Update**:
   - Update each cluster centroid \( \mu_j \) by taking the mean of all data points assigned to it:
     \[ \mu_j = \frac{1}{\text{count}(C_j)} \sum_{x \in C_j} x \]

4. **Convergence**:
   - Repeat steps 2 and 3 until convergence, i.e., when the cluster assignments no longer change significantly.

### Applications:
- Customer segmentation, image compression, etc.

## Hierarchical Clustering

Hierarchical Clustering creates a hierarchy of clusters by recursively merging or splitting data points based on their similarity.

### Methodology:
1. **Distance Measure**:
   - Define a distance metric (e.g., Euclidean distance, Manhattan distance) to quantify the dissimilarity between data points.

2. **Linkage Criteria**:
   - Choose a linkage criterion (e.g., single-linkage, complete-linkage, average-linkage) to determine the distance between clusters.

3. **Hierarchy Construction**:
   - Merge or split clusters based on the chosen linkage criterion until a dendrogram representing the hierarchy of clusters is formed.

### Applications:
- Phylogenetic tree construction, document clustering, etc.

## Principal Component Analysis (PCA)

Principal Component Analysis is a dimensionality reduction technique that projects high-dimensional data onto a lower-dimensional subspace while preserving the maximum variance.

### Methodology:
1. **Covariance Matrix**:
   - Compute the covariance matrix \( \Sigma \) of the data.

2. **Eigenvalue Decomposition**:
   - Perform eigenvalue decomposition on the covariance matrix to obtain eigenvectors \( \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_d \) and corresponding eigenvalues \( \lambda_1, \lambda_2, \ldots, \lambda_d \).

3. **Principal Components**:
   - Select the top \( k \) eigenvectors corresponding to the \( k \) largest eigenvalues as the principal components.

### Applications:
- Feature extraction, data visualization, etc.

## Apriori Algorithm for Association Rule Mining

The Apriori Algorithm discovers frequent itemsets and association rules from transactional datasets.

### Methodology:
1. **Frequent Itemset Generation**:
   - Generate frequent itemsets by iteratively applying the Apriori property:
     - A subset of a frequent itemset must also be frequent.

2. **Association Rule Generation**:
   - Extract association rules from frequent itemsets by defining minimum support and confidence thresholds.

### Applications:
- Market basket analysis, recommendation systems, etc.

## t-SNE (t-distributed Stochastic Neighbor Embedding)

t-SNE is a nonlinear dimensionality reduction technique that emphasizes the local structure of data by preserving pairwise similarities.

### Methodology:
1. **Pairwise Similarities**:
   - Compute pairwise similarities between data points in high-dimensional space using Gaussian kernel:
     \[ p_{ij} = \frac{\exp(-||\mathbf{x}_i - \mathbf{x}_j||^2 / 2 \sigma^2)}{\sum_{k \neq l} \exp(-||\mathbf{x}_k - \mathbf{x}_l||^2 / 2 \sigma^2)} \]

2. **Student's t-distribution**:
   - Model pairwise similarities in low-dimensional space using Student's t-distribution:
     \[ q_{ij} = \frac{(1 + ||\mathbf{y}_i - \mathbf{y}_j||^2)^{-1}}{\sum_{k \neq l} (1 + ||\mathbf{y}_k - \mathbf{y}_l||^2)^{-1}} \]

3. **Optimization**:
   - Optimize the low-dimensional embedding \( \mathbf{Y} \) to minimize the Kullback-Leibler divergence between \( P \) and \( Q \):
     \[ C = \sum_{i} KL(P_i || Q_i) = \sum_{i} \sum_{j \neq i} p_{ij} \log \frac{p_{ij}}{q_{ij}} \]

### Applications:
- Visualization of high-dimensional data, clustering analysis, etc.

## Conclusion

Unsupervised learning algorithms are indispensable for uncovering hidden patterns and structures within unlabeled data. By understanding the methodologies, applications, and mathematical formulations of K-Means Clustering, Hierarchical Clustering, Principal Component Analysis (PCA), Apriori Algorithm, and t-SNE, practitioners can effectively analyze and explore datasets in various domains.