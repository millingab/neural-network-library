# neural-network-library
Simple neural network library made solely using python+numpy. I pursued this project purely for educational purposes. I recommend you to use some other framework if you are looking for a machine learning library. 

## Characteristics
* Fully connected feed forward neural network with as many hidden layers as needed, of any size.
* Implements backpropagation
* Uses gradient descent for optimization
* Uses Sum Squared Error cost function
* Uses the sigmoid activation function

## How to use
1. Create an instance  
  `nn = NeuralNetwork()`
2. Add layers  
  The first input layer is created automatically  
  `nn.add_layer(shape=(input_dim1, output_dim1))`  
  `nn.add_layer(shape=(input_dim2, output_dim2))`
3. Train  
  `nn.train(features, targets, num_epochs, learning_rate)`
4. Predict  
  `nn.predict(features)`
  
The `nn.train()` method has an optional parameter called `stop_accuracy`. At the end of each epoch the mean loss is calculated and if it is under the specified threshold than the training stops. This avoids training longer than necessary. By looking at the number of epochs needed to reach the threshold, it gives us a good metric as to the performance of our hyperparameters.

## Example: XOR function
The Jupyter Notebook shows how the network can be used to approximate the XOR function using a 3-layer neural network. We attempt to find the optimal network dimensions and the optimal learning rate.

![Error](https://github.com/millingab/neural-network-library/blob/master/example/error_rate.png)
![Optimization](https://github.com/millingab/neural-network-library/blob/master/example/optimization.png)

## Dependencies
* Numpy
