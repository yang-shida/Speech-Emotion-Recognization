# EEL4773_Team_Final_Project

## Training the Models

In our train.ipynb file, scroll down past all of the cells that define our training functions. The first cell after def train will load our data into data_training and the labels in labels_training. The following cell splits the data into training and test data. The next cell runs our train function which  trains the 20 cnn models and the knn model and saves those models for easy access into .h5 files.

## Testing the Models

The test.ipynb has a test function that can be run. If you scroll down to the last cell, the cell will run the test function using the previously generated test set. The test set functions by processing all of the training data with MFCC and SFTF for KNN and reading the prediction results. The ensemble learning takes the 3 highest predicted labels from CNN and sees if the highest exceeds a threshold value. If the highest exceeds the threshold, that label is the final prediction. If the threshold is not exceeded, the final label is picked from whichever of the 3 highest labels agrees with the KNN prediction.
