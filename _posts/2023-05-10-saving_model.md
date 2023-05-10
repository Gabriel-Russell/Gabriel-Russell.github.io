# Saving a basic fastai model

In this lesson of the fastai course, there is a simple example provided for how to save a trained model for further deployment.
This method seems very similar to other ways I have previously learned how to save models such as machine learning models and for deployment afterwards.

The basic steps outlined include:
1. Downloading and decompressing dataset
2. Creating **'DataLoaders`**
3. Training the model
4. The finalling exporting the trained model using the following line

```python
MODEL.export('model.pkl')
```

Where *MODEL* is the variable that holds all the model information that has just been trained and saves it with the name *'model.pkl'*.
