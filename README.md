# Complete end-to-end Workflow for a Diabetes Prediction Deep Learning Project

The provided code demonstrates a complete end-to-end workflow for a diabetes prediction deep-learning project. It involves data exploration, preprocessing, model creation, training, evaluation, and saving the trained model for future use. The TensorFlow library allows for efficient model iteration, and the addition of EarlyStopping and batch size further enhances model training and generalization performance. Here's a description of each step:

1. First Look at Data: The code begins by loading the diabetes dataset and displaying some basic information about the dataset using the def function created by me. This provides an overview of the info, shape, data types, statistical evaluation, and the number of non-null values.

2. Change Categorical to Numerical Data: The input columns in the dataset, are converted from categorical to numerical data. This is achieved by mapping the inputs to make them suitable for model training.

3. Split Data into Test, Validation, and Training Sets: The dataset is split into three sets: a training set, a validation set, and a test set. 

4. Creating the Deep Learning Model: The deep learning model is created using TensorFlow's `Sequential` API. It consists of three layers: two dense hidden layers with ReLU activation, and one output layer with a sigmoid activation function to predict the binary outcome (diabetes or no diabetes). The model is compiled with the Adam optimizer and binary cross-entropy loss function for binary classification. Model training is performed using the `fit()` function, and an EarlyStopping callback is added to prevent overfitting by monitoring the validation loss during training.

5. Finding Test Loss and Accuracy: After training the model, its performance is evaluated on the test set using the `evaluate()` function. This calculates the test loss and test accuracy, providing an indication of how well the model generalizes to unseen data.

7. Plotting Training and Validation Loss: The code includes a plot of the training and validation loss over the epochs. This visualization helps to monitor the model's performance during training and identify potential overfitting or underfitting.

8. Saving the Trained Model and Predicting New Data: The trained model is saved to a file using the `save()` function. This allows you to reuse the model for future predictions without retraining. Finally, an example of new data is prepared, scaled, and fed into the trained model for prediction.

