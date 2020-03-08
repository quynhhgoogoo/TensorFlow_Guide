# TensorFlow_Guide
Follow tensorflow for begginers tutorials with provided datasets

### Layers inside neural networks
Layers = basic building blocks inside neural networks<br>
#### First layer: tf.keras.layers.Flatten
- transform format of images: from n-dimensional array to one dimension array
- unstacking rows of pixels in image and lining them up
- has no parameters
- JUST REFORMATS THE DATA

#### Second Layer: tf.keras.layers.Dense
- densely/fully connected neural layers
- each node contains a score that indicates the probability that input belongs to one of the provided classes (classification)

### Compile the model
- <b>Loss function: </b> measures how accurate the model is during training. One should minize this function to steer the model in right direction
- <b>Optimizer:</b> how the model is updated based on its data and its loss function
- <b>Metrics</b>: Monitor the training and testing step

### Train the model
1. Feed training data to model.
2. Model learns to associate images and labels
3. Ask model to make predictions about test sets
4. Verify that the predictions match the labels

#### Feed the model
- model.fit: fits model to training data
- epoch: epoch = 1 when we fits the whole modek to training data at once
 <br>epoch = 10 when we divide the whole model into 10 portions and fit them inside training data 10 times<br>
```model.fit(train_images, train_labels, epoch=10)```

#### Make predictions
- Attachs a softmax layer to convert logits to probabilities -> easier to interpret.
- <b>logits</b>: vector of raw (non-normalized) predictions that a classification model generates.

#### Verify predictions and use the train models
