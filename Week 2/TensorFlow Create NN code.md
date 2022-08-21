### How to create neural network and train it in Tensorflow
**Step 1: Create the model**
```
import tensorflow as tf
from tensorflow.keras import Sequential
from tensorflow.keras.layers import Dense

model = Sequential([
    Dense(units = 25, activation = 'sigmoid'),
    Dense(units = 15, activation = 'sigmoid'),
    Dense(units = 1, activation = 'sigmoid')
])

```
**Step 2: Specifying loss and cost function to be optimized**
```
# for binary classification
model.compile(loss = BinaryCrossentropy())

# for regression problem
model.compile(loss = MeanSquaredError())
```
**Step 3: Gradient Descent**
```
# this code use backward propagation underlying at behind
model.fit(X, Y, epochs = 100)
```
