# Best Image models

In this lesson of the fastai course, I have learnt a little bit about the difference image models our there that are available and the variation in performances for some of these. 
This course implements the use of [Pytorch Image Models](https://timm.fast.ai/) which is a vast library of pre-trained computer vision models. 

In this example, some data is imported and used as a basis to look at the inference performance of several families of models. 

## Inference Performance

Whereby:
- The x axis represents the amount of seconds taken (**log scale**)
- The y axis is the accuracy on Imagenet
- The size of the bubble is proportional to the size of images used in testing
- The color shows what *family* the architecture is from

![](/images/inference_graph_1.jpg) 

From here, a smaller subset of the models were taken and plotted, only keeping a single key model from each family that look the best in the plot. 
Below is the graph that was produced after doing so.

![](/images/inference_graph_2.jpg) 

Some interesting things to note were that the **levit** family models are extremely fast for image recognition, shown by their position on the graph being to the far left of the x axis,
as well as one of the most accurate models amongst the others. I found it quite interesting learning why this is so, being that **levit** family models are hybrid of the best ideas from 
CNNs (Convolutional Neural Networks) and transformers, therefore getting the benefit of each.


## Training Performance 

It was also quite interesting to see the difference between the inference performance and training performance of this subset of family models.
As shown below.

![](/images/training_graph.jpg)

I noticed that while there were slight differences, there were very similar trends between the inference and training performance for these chosen family models.

Last thing to note, being that speeds for these processes heavily depends on the hardware you are using. Such that running these models on anything other than a modern **NVIDIA GPU** may result in different performances.


