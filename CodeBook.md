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
  
  ###PART 1: Data Extraction
PART 1 of the R Script run_analysis -
Downloads the zip file and saves it as GACDataCProj.zip in the working directory
Unzips GACDataCProj.zip to the working directory
Directory “UCI HAR Dataset” contains all files need for running the R Script

###PART 2: Joining tables to create a master dataset
PART 2 of the R script run_analysis joins the test and training datsets, adds column names, activity labels and subject list
2.1 creates a vector of column names from features.txt

###PART 3: Extracts only the measurements on the mean and standard deviation for each measurement and adds descriptive activity names to name the activities in the data set
Part 3 of the R Script run_analysis (Please Note: This portion of the script utilizes the dplyr package) -
3.1 Subsets the data master created in 2.4 based on the column names containing mean and standard deviation while retaining the Label and Subject columns
3.2 Further subsets the dataset created in 3.1 to exclude columns containing Mean Frequencies which is a weighted average of the frequency components and not a straught arithmetic mean
3.3 Reads the activity list table and changes the column names to match column names in the meansd and datamaster datasets
3.4 Adds descriptive activity labels from activiylist to the meansd dataset to create the meansd_act dataset

###PART 4: Labels the data set with descriptive variable names wherever approrpiate
Part 4 of the R Script run_analysis -
Subsititutes specific character strings in the column names of the dataset meansd_act with more descriptive labels

###PART 5: Creates a second, independent tidy data set with the average of each variable for each activity and each subject
Part 5 of the R script run_analysis does the following (Please Note: This portion the script requires the dplyr and tidyr packages) -
Creates a text file TidyData.txt in the workling directory that gives a grouped mean for all selected features by activity and subject
