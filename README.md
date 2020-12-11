# EEL4773_Team_Final_Project

## Required Dependencies
- numpy
- librosa
- tensorflow
- keras
- sklearn
- pickle

## Training the Models

### File: Train.ipynb
### Steps to run: 
- Load data
```
data_training = np.load('data_training.npy')
labels_training = np.load('labels_training.npy')
```
- Call function: the first parameter is the training data, the second parameter is the training label
```
train(data_training, labels_training)
```
- The train function will run, you will see on screen the progress when training each ensemble learner. A folder called Ensemble_Learners will be created to store the models. The KNN model will be stored in a file called model_knn. Below is the example on-screen output:
```
Training ensemble learners...
Input audio shape:  (1920, 100000)
Performing data augmentation (adding noise)...
Training audio shape:  (3840, 100000)
Extracting MFCC feature...
MFCC feature shape:  (3840, 13, 196)
Training model number  0
Training model number  1
Training model number  2
Training model number  3
Training model number  4
Training model number  5
Training model number  6
Training model number  7
Training model number  8
Training model number  9
Training model number  10
Training model number  11
Training model number  12
Training model number  13
Training model number  14
Training model number  15
Training model number  16
Training model number  17
Training model number  18
Training model number  19
Training knn...
Extracting MFCC feature...
Extracting STFT feature...
Training KNN model...
K-NN training completed
```

## Testing the Models

### File: Test.ipynb
### Steps to run: 
- Load data
```
X_test = np.load('data.npy')
y_test = np.load('labels.npy')
```
- Call function: the first parameter is the testing data, the second parameter is the testing label. The function returns two parameters: accuracy score and predicted label.
```
acc_score, pred_label = test(X_test, y_test)
```
- The test function will run, there will be no on-screen output when it is running. But when it finishes, you will see the printed accuracy score like below.
```
0.8875
```
