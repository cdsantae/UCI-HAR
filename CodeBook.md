#Code Book
This is a description of files, data and variables used

###Feature Selection 
The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals
- tAcc-XYZ
- tGyro-XYZ

These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz.
Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise.

Similarly, the acceleration signal was then separated into body and gravity acceleration signals
- tBodyAcc-XYZ
- tGravityAcc-XYZ

using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals
- tBodyAccJerk-XYZ
- tBodyGyroJerk-XYZ

Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm
- tBodyAccMag
- tGravityAccMag 
- tBodyAccJerkMag
- tBodyGyroMag
- tBodyGyroJerkMag

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing
- fBodyAcc-XYZ
- fBodyAccJerk-XYZ 
- fBodyGyro-XYZ
- fBodyAccJerkMag
- fBodyGyroMag
- fBodyGyroJerkMag

(Note: the 'f' to indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

###Variables
The set of variables that were estimated from these signals are:
- <b>mean():</b> Mean value
- <b>std():</b> Standard deviation
- <b>mad():</b> Median absolute deviation 
- <b>max():</b> Largest value in array
- <b>min():</b> Smallest value in array
- <b>sma():</b> Signal magnitude area
- <b>energy():</b> Energy measure. Sum of the squares divided by the number of values. 
- <b>iqr():</b> Interquartile range 
- <b>entropy():</b> Signal entropy
- <b>arCoeff():</b> Autorregresion coefficients with Burg order equal to 4
- <b>correlation():</b> correlation coefficient between two signals
- <b>maxInds():</b> index of the frequency component with largest magnitude
- <b>meanFreq():</b> Weighted average of the frequency components to obtain a mean frequency
- <b>skewness():</b> skewness of the frequency domain signal 
- <b>kurtosis():</b> kurtosis of the frequency domain signal 
- <b>bandsEnergy():</b> Energy of a frequency interval within the 64 bins of the FFT of each window.
- <b>angle():</b> Angle between to vectors.

Additional vectors obtained by averaging the signals in a signal window sample. These are used on the angle() variable:
- gravityMean
- tBodyAccMean
- tBodyAccJerkMean
- tBodyGyroMean
- tBodyGyroJerkMean

###The dataset includes the following files:
- <b>'README.txt'</b>
- <b>'features_info.txt':</b> Shows information about the variables used on the feature vector.
- <b>'features.txt':</b> List of all features.
- <b>'activity_labels.txt':</b> Links the class labels with their activity name.
- <b>'train/X_train.txt':</b> Training set.
- <b>'train/y_train.txt':</b> Training labels.
- <b>'test/X_test.txt':</b> Test set.
- <b>'test/y_test.txt':</b> Test labels.

The following files are available for the train and test data. Their descriptions are equivalent. 
- <b>'train/subject_train.txt':</b> Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.

- <b>'train/Inertial Signals/total_acc_x_train.txt':</b> The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis.

- <b>'train/Inertial Signals/body_acc_x_train.txt':</b> The body acceleration signal obtained by subtracting the gravity from the total acceleration. 

- <b>'train/Inertial Signals/body_gyro_x_train.txt':</b> The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second. 
