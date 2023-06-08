# Deep Learning Model using Convolutional Neural Network (CNN)

This repository contains a Python script to create a CNN for image classification.

## Table of Contents
- [Data Loading and Exploration](#data-loading-and-exploration)
- [Data Preparation and Visualization](#data-preparation-and-visualization)
- [Model Creation and Training](#model-creation-and-training)
- [Model Evaluation](#model-evaluation)
- [Model Saving](#model-saving)

## Data Loading and Exploration

The data used is stored in CSV files: 'train.csv' and 'test.csv'. The script loads these files, explores the data briefly, and displays the first few entries of each data set.

## Data Preparation and Visualization

The script processes the images and labels from the training data, reshaping the data to the appropriate format and normalizing the pixel values. The images are visualized using matplotlib to ensure the data is loaded and processed correctly.

## Model Creation and Training

The CNN model is built using TensorFlow and Keras. It consists of three convolutional layers each followed by batch normalization and activation functions, max-pooling layers, a flatten layer, a dense layer, a dropout layer, and finally a dense layer for output. The model is wrapped with KerasClassifier for grid search, which is used to find the best hyperparameters for batch size, number of epochs, and optimizer type.

## Model Evaluation

Once the best model is selected based on grid search, it's used to make predictions on the test data. It visualizes the model's predictions on the first few test images. It also calculates and displays the test accuracy and loss. Besides, it generates a classification report, confusion matrix, and calculates ROC AUC score for multi-class classification.

## Model Saving

Finally, the best model is saved to disk for later use.

## Dependencies

The script uses the following Python libraries:
- numpy
- pandas
- matplotlib
- sklearn
- tensorflow

## Running the Script

To run the script, ensure that the above dependencies are installed in your Python environment. The script can be run from the command line using the command `Deep_Learning.ipynb`.

Before running, ensure that 'train.csv' and 'test.csv' files are available in the same directory as the script or modify the file paths in the script accordingly. After running the script, 'best_model.h5' will be saved in the same directory.

## Author

This model was created by [Oliver Ardila](https://github.com/oardilac).

## License

This project is licensed under the [MIT License](LICENSE).