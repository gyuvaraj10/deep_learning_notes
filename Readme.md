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
