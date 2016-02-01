
# This is the course project for the Getting and Cleaning Data Coursera course

**About the raw data**

Human Activity Recognition database built from the recordings of 30 subjects performing activities of daily living (ADL) while carrying a waist-mounted smartphone with embedded inertial sensors.

Data Set Characteristics: Time-Series, Multivariate
Number of Instances: 10299
Number of Attributes: 561

Data can be found in the x_test.txt. 
The activity labels are in the y_test.txt file.
The test subjects are in the subject_test.txt file.
The same holds for the training set.

**The R script, run_analysis.R, does the following:**

Download the dataset
Load the activity and feature information, training and test dataset.

Keep only those columns which reflect a mean or standard deviation
Load the activity and subject data for each dataset, and merges those columns with the dataset
Merges the two datasets
Converts the activity and subject columns into factors
Creates a tidy dataset that consists of the average (mean) value of each variable for each subject and activity pair.

The full code is in the file tidy.txt
