Data leakage, a very interesting topic. If anyone has not heard of it before and someone asked them about this, it is pretty sure that the 
answer we will get will be quite interesting. Some will say that a portion of data will be masked or removed accidentally while training.
Is it not? But here is the answer.
Sometimes when we train a model and test it, the accuracy we get is very high and no overfitting occurs. We think that the model is ready 
to be deployed and we deploy it. Boom, it fails in production. You do not get same level of performance in production as you got in testing.
This is often called data leakage.

### There are many situations where data leakage can be found. Some of them are explained here: 
#### 1. While transformation or preprocessing of data - 
        Example - While applying dimensionality reduction or transformation such as scaling the dataset, we accidentally, do it on the 
        whole data and then split it into training and testing data. For example while applying standard scaling we use the mean of
        whole data and scale it. Then split it into train and test. What happens is both train and test data become almost same. There is 
        no puspose of testing. So the right method is first split the data and then transform both train and test data separately. It is 
        explained in the notebook.
        
        
#### 2. Time series data -
        Suppose the data is in order A -> B -> C. We may accidentally train it on A and C. Here also a data leakage problem can occur.
        
        
#### 3. When many data points are duplicate.
        
        
        
        
