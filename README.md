# Getting-And-Cleaning-Data
project (week4)

## Goal of the Project
The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. 
The goal is to prepare tidy data that can be used for later analysis. 


## Files 
* README.md  -- The file you are reading:  explains how all of the scripts work and how they are connected.
* coodbook.md -- gives information about the data and steps to run the project.
* MeanData.txt -- a tidy dataset that contains mean of each sample for each activity and each subject.
* run_analysis.R  -- R script for running all functions to fulfil this project tasks:
    1. Merges the training and the test sets to create one data set.
         * Using download.file() together with unzip() function to download the zip file from the website as required in the announcement.
         * Using read.table() function to load "X_train.txt", "y_train", "subject_train" in train directory and "X_test", "y_test",    "subject_test" into R. 
         * Using rbind() and cbind() functions to merge all train and test data together.
    2. Extracts only the measurements on the mean and standard deviation for each measurement.
          * Using read.table() function to load "features.txt" into R. 
          * Using grep() function to find the indexes with "mean()" and "sd()". 
          * Select all relevant columns and set the columns name using the selected features name.
    3. Uses descriptive activity names to name the activities in the data set.
        * Using read.table() function to load "activity_labels.txt" into R. 
        * Using factor() function with arguments "levels = " and "labels = " to replace the numbers to activity names.
    4. Appropriately labels the data set with descriptive variable names.
        * Using gsub() function to replace all characters I think they are needed to replace.
    5. From the dataset in iv., creates a second, independent tidy dataset with the average of each variable for each activity and each subject.
        * Using group_by() and summarise_each() functions in dplyr package to calculate all means for each activity and wach subject.
    
 
