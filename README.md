## Project Objective

This project explores two approaches for blink prediction using pairs of eye images. Given that the task involves image data, the models are based on Convolutional Neural Networks (CNNs).

1. **Custom CNN Construction:**
   - Build and train a Convolutional Neural Network (CNN) from scratch. The network includes an input layer, several convolutional and pooling layers, a flatten layer, and two fully-connected layers. The final fully-connected layer serves as the output layer with a single neuron, suitable for binary classification.

2. **Transfer Learning with Pre-trained CNN:**
   - Utilize a pre-trained CNN and adapt it to the task through transfer learning. The chosen model is DenseNet121, pre-trained on ImageNet, selected for its compact size and relatively small number of parameters compared to other pre-trained networks.

Both approaches use Binary Focal Cross-Entropy as the loss function, which is effective for imbalanced datasets by penalizing easier-to-predict instances less and harder ones more, which is particularly useful for closed-eye prediction.

The optimization algorithm used is Adam.
