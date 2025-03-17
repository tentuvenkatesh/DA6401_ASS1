All the solutions with the codes and outputs for this assigenment will be there in "DL_ASS1(2).ipynb".

Below i am giving some best summary:

Question-1:
Download the fashion-MNIST dataset and plot 1 sample image for each class as shown in the grid below. Use from keras.datasets import fashion_mnist for getting the fashion mnist dataset.

Question-2:
Implement a feedforward neural network which takes images from the fashion-mnist data as input and outputs a probability distribution over the 10 classes.
Your code should be flexible such that it is easy to change the number of hidden layers and the number of neurons in each hidden layer.

Question-3:
Implement the backpropagation algorithm with support for the following optimisation functions 
sgd
momentum based gradient descent
nesterov accelerated gradient descent
rmsprop
adam
nadam
(12 marks for the backpropagation framework and 2 marks for each of the optimisation algorithms above)
We will check the code for implementation and ease of use (e.g., how easy it is to add a new optimisation algorithm such as Eve). Note that the code should be flexible enough to work with different batch sizes.


Question-4:
Use the sweep functionality provided by wandb to find the best values for the hyperparameters listed below. Use the standard train/test split of fashion_mnist (use (X_train, y_train), (X_test, y_test) = fashion_mnist.load_data()).  Keep 10% of the training data aside as validation data for this hyperparameter search. Here are some suggestions for different values to try for hyperparameters. As you can quickly see that this leads to an exponential number of combinations. You will have to think about strategies to do this hyperparameter search efficiently. Check out the options provided by wandb.sweep and write down what strategy you chose and why.
number of epochs: 5, 10
number of hidden layers:  3, 4, 5
size of every hidden layer:  32, 64, 128
weight decay (L2 regularisation): 0, 0.0005,  0.5
learning rate: 1e-3, 1 e-4 
optimizer:  sgd, momentum, nesterov, rmsprop, adam, nadam
batch size: 16, 32, 64
weight initialisation: random, Xavier
activation functions: sigmoid, tanh, ReLU
wandb will automatically generate the following plots. Paste these plots below using the "Add Panel to Report" feature. Make sure you use meaningful names for each sweep (e.g. hl_3_bs_16_ac_tanh to indicate that there were 3 hidden layers, batch size was 16 and activation function was ReLU) instead of using the default names (whole-sweep, kind-sweep) given by wandb.


Question-5:
We would like to see the best accuracy on the validation set across all the models that you train.
wandb automatically generates this plot which summarises the test accuracy of all the models that you tested. Please paste this plot below using the "Add Panel to Report" feature


Question-6:
Based on the different experiments that you have run we want you to make some inferences about which configurations worked and which did not. 
Here again, wandb automatically generates a "Parallel co-ordinates plot" and a "correlation summary" as shown below. Learn about a "Parallel co-ordinates plot" and how to read it.
By looking at the plots that you get, write down some interesting observations (simple bullet points but should be insightful). You can also refer to the plot in Question 5 while writing these insights. For example, in the above sample plot there are many configurations which give less than 65% accuracy. I would like to zoom into those and see what is happening. 
I would also like to see a recommendation for what configuration to use to get close to 95% accuracy.


Question-7:
For the best model identified above, report the accuracy on the test set of fashion_mnist and plot the confusion matrix as shown below. More marks for creativity (less marks for producing the plot shown below as it is)

Question-8:
In all the models above you would have used cross entropy loss. Now compare the cross entropy loss with the squared error loss. I would again like to see some automatically generated plots or your own plots to convince me whether one is better than the other.
