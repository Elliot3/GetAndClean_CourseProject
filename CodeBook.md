# CodeBook

## Data source

This dataset is derived from the "Human Activity Recognition Using Smartphones Data Set" which was originally made avaiable here: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Included in the Data Source are:
- activity_labels.txt: Relates activity labels to ids
- features_info.txt: Explains the features selected for the exercise
- features.txt: A file of all associated features
- README.txt: A README file explaining the collection of files
- test/subject_test.txt: Subjects who performed the activity
- test/X_test.txt: The test set for the data
- test/y_test.txt: Labels for the test set
- train/subject_train.txt: Subjects who performed the activity
- train/X_train.txt: Training set for the data
- train/y_train.txt: Labels for the training set

## Miscellaneous Information

Aside from the variables identifed below, the following are also present:
- activity_label: This relates an activity type to a particular subject (Walking, Walking_Upstairs, Walking_Downstairs, Sitting, Standing, Laying)
- subject_id: This acts as a numeric identifier for each individual in the population (1-30)

## Feature Selection 

The following excerpts were taken from the README file from the original data set

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

The reasoning behind my selection of features is that the assignment explicitly states "Extracts only the measurements on the mean and standard deviation for each measurement."
To be complete, I included all variables having to do with mean or standard deviation.

The following signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

* tBodyAcc-XYZ
* tGravityAcc-XYZ
* tBodyAccJerk-XYZ
* tBodyGyro-XYZ
* tBodyGyroJerk-XYZ
* tBodyAccMag
* tGravityAccMag
* tBodyAccJerkMag
* tBodyGyroMag
* tBodyGyroJerkMag
* fBodyAcc-XYZ
* fBodyAccJerk-XYZ
* fBodyGyro-XYZ
* fBodyAccMag
* fBodyAccJerkMag
* fBodyGyroMag
* fBodyGyroJerkMag

As it relates to this exercise, the following variables were estimated from the previously discussed signals.

* mean(): Mean value
* std(): Standard deviation

Additional vectors obtained by averaging the signals in a signal window sample. These are used on the angle() variable:

* gravityMean
* tBodyAccMean
* tBodyAccJerkMean
* tBodyGyroMean
* tBodyGyroJerkMean

## Units Used

- Any acceleration signal from the smartphone accelerometer is measured in 'g' (Standard Gravity)
- Any body acceleration (also in standard gravity) is obtainted by subtracting gravity from the total acceleration
- Any angular velocity vector measurement by the gyroscope is measured in radians/second 
