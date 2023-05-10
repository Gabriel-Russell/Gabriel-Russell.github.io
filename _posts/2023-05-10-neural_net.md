# How a Neural Network really works

At the most basic high level component of what a Neural Network is, it is a mathematical function that performs the following three functions:

1. Multiples each input by a number of values (known as *parameters*)
2. Adds these up for each group of values
3. Replaces the negative numbers with zeros

The combination of these three steps forms a single layer of the neural net, whereby these are then repeated, using the outputs of the previous layer to form the inputs of the next layer.
Rather than just feeding in random numbers such that it doesn't really learn anything, we can change the parameters to make it better using **gradient descent**.

## Gradient Descent
This method essentially involves adding some random noise into the data, and then performing gradient descent to recreate the original function from the data (prior to noise).
The example used was attempting to recreate a quadratic function that was originally created.

The graph below shows the original quadratic function (*y = 3x<sup>2</sup> + 2x + 1*)
![](/images/quadratic_graph.jpg)

And after some noise was added, the graph now looks like the following.
![](/images/noisy_quadratic.jpg)

The main idea for finding what quadratic function fits this noisy pot of points is to change parameters of a neural network to find the best values that fit for this case using the mean absolute error between a data point and a point on the curve.
Calculus forms the basis for how each of these parameters are determined, to know whether or not a parameter should be increased or decreased by measuring rates of change of a function.

## Automating Gradient Descent

Some main takeaways from the code listed for automating this process are as follows.
- The **`mae()`** function is used to calculate the **Mean Absolute Error**.
- The **`requires_grad_()`** function calculates gradients for input parameters after forming a single tensor. 
- The main thing to be minimised is the *loss* of a function.
- The **`backward()`** function is used to calculate the gradients.
- The **`with torch.no_grad()`** function is used to wrap a calculation into new parameters.

## How Neural Nets approximate any given function
The way  neural network fundamentally do this are two key tricks:

1. Matrix Multiplication
2. Replacing all negative numbers with zero



