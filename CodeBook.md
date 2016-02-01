#Getting and Cleaning Data
##Code Book for the Course Project.

###Project description
Given some sample data, combine the test and training sets. The data contains 
30 subjects, each performing 6 activities, along with variables measuring and 
calculating various values during each activity. The goal is to create a 
summary data set of the mean values for the means and standard deviation 
columns in the original data for each combination of subject and activity.


### Explanation of each file
 
  `features.txt`: Names of the 561 features.
  `activity_labels.txt`: Names and IDs for each of the 6 activities.
 
  `X_train.txt`: 7352 observations of the 561 features, for 21 of the 30 volunteers.
  `subject_train.txt`: A vector of 7352 integers, denoting the ID of the volunteer related to each of the observations in `X_train.txt`.
  `y_train.txt`: A vector of 7352 integers, denoting the ID of the activity related to each of the observations in `X_train.txt`.
 
  `X_test.txt`: 2947 observations of the 561 features, for 9 of the 30 volunteers.
  `subject_test.txt`: A vector of 2947 integers, denoting the ID of the volunteer related to each of the observations in `X_test.txt`.
  `y_test.txt`: A vector of 2947 integers, denoting the ID of the activity related to each of the observations in `X_test.txt`.
  
  PART 1: Data Extraction
PART 1 of the R Script run_analysis -
Downloads the zip file and saves it as GACDataCProj.zip in the working directory
Unzips GACDataCProj.zip to the working directory
Directory “UCI HAR Dataset” contains all files need for running the R Script
