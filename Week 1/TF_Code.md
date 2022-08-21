### Tensor flow Code for implementing a dense neural network

<figure>
    <center>
    <img src="Roasting Coffee Examples.png" alt="Examples of Neural Network Architecture" style="width:100%">
    <figcaption>Examples of Neural Network Architecture</figcaption>
</figure>

**Code**
```
x = np.array([[200.0, 17.0]])

# Dense is the name of the layer of the neural network
layer_1 = Dense(units = 3, activation = 'sigmoid')

# To Compute the value of a1, apply the function to the x-values
a1 = layer_1(x)
# a1 is a matrix of 1 x 3 matrix
# it is of tensor data type

# converting tensor data type into numpy data type
a1.numpy()

layer_2 = Dense(units = 1, activation = 'sigmoid')

a2 = layer_2(a1)
# one by one matrix, 2D array with one row and one column

a2.numpy()

# Classification Threshold
if a2 > 0.5:
    y_hat = 1
else:
    y_hat = 0
```

- Unfortunately, numpy and tensorflow represents and handles data structure in two different manner for linear algebra

<figure>
    <center>
    <img src="Numpy.Array.1.png" alt="Numpy Array Creation" style="width:100%">
    <figcaption>Numpy Array Creation</figcaption>
</figure>

- one dimensional vector is not the same as two dimensional matrix

<figure>
    <center>
    <img src="Numpy.Array.2.png" alt="Numpy Array Creation" style="width:100%">
    <figcaption>Numpy Array Creation</figcaption>
</figure>

- use one dimensional vector for creating random value for linear regression prediction
- use two dimensional matrix for feature vector creation
- usually people load data and do data manipulation in numpy array and feed the numpy array into a tensor flow created neural network, where it converts into tensor data types and run efficiently internally, and output tensor data type, if you need an output in numpy format, you need to convert the tensor output back to numpy array again

### To build neural network in tensor flow in an inplicit manner
- previous one is the explicit manner where only forward propagation is done sequentially in one line of code for one time
- to implement forward propagation and learning at the same time

```
# to sequentially string the neural network created together
layer_1 = Dense(units=3, activation="sigmoid")
layer_2 = Dense(units=3, activation="sigmoid")
model = Sequential([layer_1, layer_2])

# An alternate way of creating a layer


model = Sequential([layer_1 = Dense(units=3, activation="sigmoid"), 
        layer_2 = Dense(units=3, activation="sigmoid")])

# created training data
x_train = np.array([[], [], ..., []])
y_train(targets) = np.array([0, 1, 0, 1, 1])

model.compile(...) # some parameters to be put, which will be elaborated in next week
model.fit(x, y)

# to make new prediction
model.predict(x_new) 
# the forward propagation will be implemented by the network by itself by calling this line of code
```

### Extra Notes: Caveat on AI
- AI is branched into Artificual Narrow Intelligence (ANI) and Artificial General Intelligence (AGI)
- ANI has progressed a lot and most of the breakthrough in the world of machine learning nowadays are coming from this area, where the AI model or system is only particularly good at doing a single tasks, creating a lot of (economic and useful) values to humankind
- AGI is almost can do anything that a human can do easily and there is still at least decades to go to develop a breakthrough in AGI
    - each artificial neuron is too simplified version of biological neuron
    - we still almost do not know how our brain and neural system works
    - but due to neuroplasticity and the adaptability of our brain, we are having hope for AGI