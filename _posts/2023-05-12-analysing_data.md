# Model result analysis

During my attempt to analyse the results of my model performance for classifying 10 different animals using fastai functions, I have learnt a little bit about different techniques typically used.
For analysing results of a model, multiclass loss functions, t-SNE's and Confusion matrices are typically used. 

## Multiclass Loss functions

A loss function is a method to evaluate how well an algorithm models a chosen dataset. For this case of classifying many different animals,
a multiclass loss function is used to provide metrics on how well the algorithm chosen models all 10 difference classifications of animals chosen.
Loss functions that output a **higher** number indicate the predictions are **inaccurate**. Loss functions that 
output a **lower** number indicate the prediction is **accurate**.

## t-SNE

t-SNE stands for T-distributed Stochastic Neighbourhood Embedding. This is an unsupervised Machine learning algorithm used to visualise the structure of high dimensional data in 2 or 3 dimensions.
This takes the form of a simple scatter plot such as the one below. The following plot was sourced from DataTechNotes that used t-SNE for visualising the  MNIST dataset.
![](/images/t_SNE_image.jpg)

## Confusion Matrices
A confusion matrix is a visual representation that determines the accuracy of actual vs predicted values from the output of a model.
A confusion matrix will contain a row/column for each classification used, that will indicate the percentage or number of true positives/negatives and false positives/negatives present.
If a model is extremely accurate, the ideal scenario will present a diagonal from top left to bottom right of the confusion matrix where these percentages are close to or exactly 100% or equal to the number of inputs tested.
The following image is a simple example of a confusion matrix. 
![](/images/confusion_matrix.jpg)

Overall, these are three different methods that all contribute to data and performance analysis to give a user an indication of what their model is like.
