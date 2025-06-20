**Activation Function Selection**:
1. For output layers it is recommended to use sigmoid function and for others we can use tan(h).
2. For hidden layers, if you are not sure which activation function to use, just use ReLu function = max(0, x)
```
Example:
model = keras.Sequential([
    keras.layers.Flatten(input_shape= (28,28)),
    keras.layers.Dense(100, activation='relu'),
    keras.layers.Dense(10, activation='sigmoid')
])

model.compile(optimizer='adam', loss=keras.losses.CategoricalCrossentropy(), metrics=['accuracy'])
model.fit(X_train, keras.utils.to_categorical(y_train, num_classes=np.max(y_train)+1), epochs=10)
```
3. Activation Functions 
```
ReLU(z) = max(0,z)
Leaky ReLU(x) = max(0.1x,x)
sigmoid(z) = 1/1+e^-z
tanh(z) = (e^z-e^-z)/(e^z+e^-z)
```
Mathematical Concepts:
[mathisfun.com](https://www.mathsisfun.com/)

**Loss.Error**:
Loss is used in neural network training. Available Losses  are https://www.tensorflow.org/api_docs/python/tf/keras/losses
 
Absolute Error: abs(y-y^)
Total Error: Sum(abs(y1-y1^)+.....abs(yn-yn^))
Mean Absolute Error (MAE) = Total Error/n - Cost Function

**Notes**:
1. For logistic regression we use log loss or binary cross entropy function and do not use mse due to it's non-convex nature.

**Gradient Descent**
Using this, we can find the parameters of linear equations. Example y=mx+c, we can find m and c using Gradient descent algo. Helps in training the model to find the best fit values.
