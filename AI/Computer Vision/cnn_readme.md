# Convolutional Neural Networks (CNNs)

Convolutional Neural Networks (CNNs) are deep learning architectures designed for processing structured grid data, such as images. They have revolutionized the field of computer vision by enabling automated feature extraction and hierarchical learning. This README provides a comprehensive overview of CNNs, including their key components, operations, and mathematical formulations.

## Convolutional Layers

Convolutional layers are the building blocks of CNNs and are responsible for feature extraction. Each convolutional layer consists of a set of learnable filters (also called kernels) that are convolved with the input image to produce feature maps.

### Operation
Given an input image \( I \) and a filter \( W \), the convolution operation is defined as follows:

\[ F(x, y) = \sum_{i=-a}^{a} \sum_{j=-b}^{b} I(x+i, y+j) \cdot W(i, j) + b \]

where \( F \) is the feature map, \( (x, y) \) are the spatial coordinates, \( a \) and \( b \) are the extents of the filter, and \( b \) is the bias term.

### Activation
The output of the convolutional operation is often passed through an activation function, such as the Rectified Linear Unit (ReLU), to introduce non-linearity:

\[ A(x, y) = \text{ReLU}(F(x, y)) \]

## Pooling Layers

Pooling layers downsample feature maps to reduce spatial dimensions and computational complexity while retaining important features.

### Max Pooling
Max pooling selects the maximum value within a local region:

\[ P(x, y) = \max_{i,j} \left( F(x + i, y + j) \right) \]

### Average Pooling
Average pooling computes the average value within a local region:

\[ P(x, y) = \frac{1}{(2a+1)(2b+1)} \sum_{i=-a}^{a} \sum_{j=-b}^{b} F(x+i, y+j) \]

## Fully Connected Layers

Fully connected layers connect every neuron in one layer to every neuron in the next layer, enabling high-level feature learning and classification.

### Operation
Given a flattened feature vector \( \mathbf{x} \) and weights \( \mathbf{W} \), the operation of a fully connected layer is defined as:

\[ \mathbf{z} = \mathbf{Wx} + \mathbf{b} \]

where \( \mathbf{z} \) is the output vector and \( \mathbf{b} \) is the bias vector.

### Activation
The output of the fully connected layer is often passed through an activation function, such as the softmax function for classification tasks:

\[ \text{softmax}(\mathbf{z})_i = \frac{e^{z_i}}{\sum_{j=1}^{N} e^{z_j}} \]

where \( N \) is the number of classes.

## Training CNNs

CNNs are trained using backpropagation and gradient descent to minimize a loss function, such as categorical cross-entropy for classification tasks or mean squared error for regression tasks. The weights of the network are updated iteratively using the gradient of the loss function with respect to the network parameters.

### Backpropagation
Backpropagation computes the gradient of the loss function with respect to each parameter in the network using the chain rule of calculus. The gradients are then used to update the parameters in the direction that minimizes the loss.

### Optimization Algorithms
Optimization algorithms, such as stochastic gradient descent (SGD), Adam, or RMSProp, are used to update the parameters efficiently. These algorithms adjust the learning rate and momentum of the updates to accelerate convergence.