# Getting And Cleaning Data Project
This gives the relevant information about the data and steps to run the project. It indicates all the variables and summaries calculated.

## Data
The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. 
A full description is available at the site where the data was obtained:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Here are the data for this project:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

## Variables
* "X_train.txt", "y_train.txt", "subject_train.txt" -- contain information about training data.
* "X_test.txt", "y_test.txt", "subjuect_test.txt" -- contain information about testing data.
* "features.txt"  -- contains names of all measurements.

## Functions for the analysis: 
*  download.file() together with unzip()  -- download the zip file from website to my machine.
*  read.table()  --  load "X_train.txt", "y_train", "subject_train" in train directory and "X_test", "y_test", "subject_test" into R.
*  rbind() and cbind()  -- to merge all train and test data together.

* read.table()   -- to load "features.txt" into R.

*  grep()   -- to find the indexes with "mean()" and "sd()".
* select all relevant columns and set the columns name using the selected features name.

*  read.table()  -- to load "activity_labels.txt" into R.

*  factor() with arguments "levels = " and "labels = "  -- to replace the numbers to activity names.

*  gsub()  -- to replace all characters (needed to replace).

* group_by() and summarise_each() in dplyr package --  to calculate all means for each activity and watch subject.

