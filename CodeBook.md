#Introduction
This CodeBook describes the variables, the data, and the transformations performed to convert the raw data into tidy data.

#Raw data
The raw data was taken from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip , which contains data collected from the accelerometers from the Samsung Galaxy S smartphone.
'subject' variable represents the ID of the test subject.
'activity' variable represents the type of activity performed when the corresponding measurements were taken.

#R Script
Script run_analysis.R performs the 5 steps described in the course project's instructions:
  1. Merges the training and the test sets to create one data set, by using the rbind() function.
  2. Extracts only the measurements on the mean and standard deviation for each measurement.
  3. Uses descriptive activity names to name the activities in the data set, by using features.txt file.
  4. Appropriately labels the data set with descriptive variable names.
  5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

#Tidy data
The output of the 5th step is the "tidy_data.txt" file in this repo, which stores the average of each variable for each activity and each subject.
It contains 180 observations of the following 69 variables:

 $ Subject                    : int  1 1 1 1 1 1 2 2 2 2 ...
 $ Activity                   : Factor w/ 6 levels "LAYING","SITTING",..: 1 2 3 4 5 6 1 2 3 4 ...
 $ tBodyAcc-mean()-X          : num  0.222 0.261 0.279 0.277 0.289 ...
 $ tBodyAcc-mean()-Y          : num  -0.04051 -0.00131 -0.01614 -0.01738 -0.00992 ...
 $ tBodyAcc-mean()-Z          : num  -0.113 -0.105 -0.111 -0.111 -0.108 ...
 $ tBodyAcc-std()-X           : num  -0.928 -0.977 -0.996 -0.284 0.03 ...
 $ tBodyAcc-std()-Y           : num  -0.8368 -0.9226 -0.9732 0.1145 -0.0319 ...
 $ tBodyAcc-std()-Z           : num  -0.826 -0.94 -0.98 -0.26 -0.23 ...
 $ tGravityAcc-mean()-X       : num  -0.9321 -0.9795 -0.9961 -0.3407 -0.0441 ...
 $ tGravityAcc-mean()-Y       : num  -0.8409 -0.9197 -0.9718 0.0618 -0.1074 ...
 $ tGravityAcc-mean()-Z       : num  -0.822 -0.939 -0.979 -0.25 -0.212 ...
 $ tGravityAcc-std()-X        : num  -0.906 -0.927 -0.939 -0.103 0.389 ...
 $ tGravityAcc-std()-Y        : num  -0.5016 -0.5174 -0.5609 -0.0557 -0.0953 ...
 $ tGravityAcc-std()-Z        : num  -0.703 -0.786 -0.813 -0.255 -0.317 ...
 $ tBodyAccJerk-mean()-X      : num  0.7431 0.8203 0.8489 0.1196 0.0157 ...
 $ tBodyAccJerk-mean()-Y      : num  0.5849 0.6828 0.685 -0.0212 -0.0437 ...
 $ tBodyAccJerk-mean()-Z      : num  0.758 0.822 0.838 0.437 0.305 ...
 $ tBodyAccJerk-std()-X       : num  -0.842 -0.946 -0.984 -0.126 0.008 ...
 $ tBodyAccJerk-std()-Y       : num  -0.984 -0.998 -1 -0.739 -0.463 ...
 $ tBodyAccJerk-std()-Z       : num  -0.948 -0.99 -0.999 -0.758 -0.813 ...
 $ tBodyGyro-mean()-X         : num  -0.905 -0.987 -0.999 -0.748 -0.724 ...
 $ tBodyGyro-mean()-Y         : num  -0.94 -0.983 -0.996 -0.424 -0.225 ...
 $ tBodyGyro-mean()-Z         : num  -0.877 -0.932 -0.974 -0.299 -0.399 ...
 $ tBodyGyro-std()-X          : num  -0.823 -0.943 -0.979 -0.252 -0.206 ...
 $ tBodyGyro-std()-Y          : num  -0.372 -0.594 -0.654 0.359 0.237 ...
 $ tBodyGyro-std()-Z          : num  -0.491 -0.399 -0.563 0.437 0.376 ...
 $ tBodyGyroJerk-mean()-X     : num  -0.402 -0.5213 -0.5895 0.0424 0.1697 ...
 $ tBodyGyroJerk-mean()-Y     : num  0.043 0.152 0.297 -0.335 -0.395 ...
 $ tBodyGyroJerk-mean()-Z     : num  0.00523 -0.05942 -0.14551 0.34841 0.36759 ...
 $ tBodyGyroJerk-std()-X      : num  -0.0323 0.041 0.1136 -0.1492 -0.31 ...
 $ tBodyGyroJerk-std()-Y      : num  0.14657 -0.00412 0.0807 0.07994 0.2763 ...
 $ tBodyGyroJerk-std()-Z      : num  0.176 0.169 0.185 -0.167 -0.121 ...
 $ tBodyAccMag-mean()         : num  -0.104 -0.129 -0.138 0.175 0.155 ...
 $ tBodyAccMag-std()          : num  0.1842 0.1851 0.1903 0.1678 0.0867 ...
 $ tGravityAccMag-mean()      : num  0.0105 -0.117 -0.0158 -0.0514 0.0377 ...
 $ tGravityAccMag-std()       : num  0.2091 0.2589 0.2799 -0.1189 0.0804 ...
 $ tBodyAccJerkMag-mean()     : num  -0.1219 -0.1171 -0.1279 0.1673 0.0878 ...
 $ tBodyAccJerkMag-std()      : num  0.09054 0.08508 0.11685 0.00262 0.02916 ...
 $ tBodyGyroMag-mean()        : num  0.00239 -0.02272 -0.10391 -0.27517 -0.2914 ...
 $ tBodyGyroMag-std()         : num  -0.0409 -0.4029 0.1284 -0.1437 -0.4542 ...
 $ tBodyGyroJerkMag-mean()    : num  -0.00933 -0.20119 -0.00543 -0.19123 -0.22554 ...
 $ tBodyGyroJerkMag-std()     : num  -0.0234 0.1183 0.2883 0.3802 0.0757 ...
 $ fBodyAcc-mean()-X          : num  -0.249 0.832 0.943 0.935 0.932 ...
 $ fBodyAcc-mean()-Y          : num  0.706 0.204 -0.273 -0.282 -0.267 ...
 $ fBodyAcc-mean()-Z          : num  0.4458 0.332 0.0135 -0.0681 -0.0621 ...
 $ fBodyAcc-std()-X           : num  -0.897 -0.968 -0.994 -0.977 -0.951 ...
 $ fBodyAcc-std()-Y           : num  -0.908 -0.936 -0.981 -0.971 -0.937 ...
 $ fBodyAcc-std()-Z           : num  -0.852 -0.949 -0.976 -0.948 -0.896 ...
 $ fBodyAccJerk-mean()-X      : num  -0.899 -0.969 -0.994 -0.977 -0.951 ...
 $ fBodyAccJerk-mean()-Y      : num  -0.91 -0.938 -0.981 -0.972 -0.938 ...
 $ fBodyAccJerk-mean()-Z      : num  -0.855 -0.95 -0.977 -0.95 -0.898 ...
 $ fBodyAccJerk-std()-X       : num  -0.28 0.768 0.87 0.869 0.876 ...
 $ fBodyAccJerk-std()-Y       : num  0.685 0.188 -0.288 -0.294 -0.27 ...
 $ fBodyAccJerk-std()-Z       : num  0.4694 0.3319 0.0097 -0.0629 -0.0465 ...
 $ fBodyGyro-mean()-X         : num  -0.236 0.843 0.961 0.947 0.936 ...
 $ fBodyGyro-mean()-Y         : num  0.692 0.205 -0.248 -0.26 -0.256 ...
 $ fBodyGyro-mean()-Z         : num  0.41387 0.32184 0.00938 -0.07849 -0.0863 ...
 $ fBodyGyro-std()-X          : num  0.248 0.225 -0.244 -0.142 -0.206 ...
 $ fBodyGyro-std()-Y          : num  -0.907 0.575 0.846 0.826 0.817 ...
 $ fBodyGyro-std()-Z          : num  0.165 -0.88 -0.862 -0.864 -0.879 ...
 $ fBodyAccMag-mean()         : num  -0.32 -0.779 -0.995 -0.986 -0.988 ...
 $ fBodyAccMag-std()          : num  -0.906 -0.972 -0.994 -0.978 -0.953 ...
 $ fBodyBodyAccJerkMag-mean() : num  -0.916 -0.944 -0.981 -0.973 -0.941 ...
 $ fBodyBodyAccJerkMag-std()  : num  -0.863 -0.954 -0.978 -0.955 -0.907 ...
 $ fBodyBodyGyroMag-mean()    : num  -0.518 -0.686 -0.886 -0.667 -0.445 ...
 $ fBodyBodyGyroMag-std()     : num  -0.554 -0.489 -1 -1 -1 ...
 $ fBodyBodyGyroJerkMag-mean(): num  -0.58 -0.626 -0.852 -0.993 -0.98 ...
 $ fBodyBodyGyroJerkMag-std() : num  -0.594 -0.53 -0.383 -0.298 -0.571 ...
 $ NA                         : num  0.609 0.543 0.404 0.383 0.63 ...