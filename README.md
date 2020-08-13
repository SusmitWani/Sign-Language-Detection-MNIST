# Sign-Language-Detection-MNIST

This is a project made by me to test my skills in building a multi class classifier to detect images and classify them into respective classes. I have used TensorFlow and Keras in this project. The summary of the neural network used is as follows. The images used as input are of shape (28, 28, 1).

```
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d (Conv2D)              (None, 24, 24, 64)        1664      
_________________________________________________________________
max_pooling2d (MaxPooling2D) (None, 12, 12, 64)        0         
_________________________________________________________________
conv2d_1 (Conv2D)            (None, 10, 10, 128)       73856     
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 5, 5, 128)         0         
_________________________________________________________________
dropout (Dropout)            (None, 5, 5, 128)         0         
_________________________________________________________________
flatten (Flatten)            (None, 3200)              0         
_________________________________________________________________
dense (Dense)                (None, 512)               1638912   
_________________________________________________________________
dense_1 (Dense)              (None, 256)               131328    
_________________________________________________________________
dense_2 (Dense)              (None, 25)                6425      
=================================================================
Total params: 1,852,185
Trainable params: 1,852,185
Non-trainable params: 0
=================================================================
```


As you can see, it is a basic model which still achieves high accuracies for both validation and test datasets. The first Conv2D layer has 64 filters with a size of (5, 5) and the second Conv2D layer has 128 filters of size (3,3). Both the Max Pooling layers have a pool size of (2,2) and no stride length. Finally, there is a droupout layer with a probability to drop a particular neuron set to 0.2 and two fully connected dense layers with 512 and 256 neurons each. The last dense layer is connected to a softmax output layer which returns the predicted index of the image.

I beleve the model can further be improved by including more layers and 
