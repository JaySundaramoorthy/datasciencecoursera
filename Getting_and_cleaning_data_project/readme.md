## Getting and Cleaning Data Project

Created by Jay Sundaramoorthy

Repo for the submission of the course project for the Johns Hopkins Getting and Cleaning Data course.

### Overview
This project serves to demonstrate the collection and cleaning of a tidy data set that can be used for subsequent
analysis. A full description of the data used in this project can be found at [The UCI Machine Learning Repository](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

[The source data for this project can be found here.](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)

### Making Modifications to This Script
Once you have obtained and unzipped the source files, you will need to make one modification to the R file before you can process the data.


### Project Summary
The following is a summary description of the project instructions
==================================
The run_analysis.R script merges data from a number of .txt files and produces a tidy data set which may be used for further analysis.

- First it checks to see if the required "reshape2" has been installed and then loads the "reshape2" package.

- It then reads all required .txt files and labels the datasets

- Consquently the appropriate "activity_id"'s and "subject_id"'s are appended to the "test" and the "training" data, which are then combined into one single data frame

- Using the "grep" function, all the columns with mean() and std() values are extracted and then a new data frame, including only the "activity_id", the "subject_id" and the mean() and std() columns, is created    

- Using the "merge" function, descriptive activity names are merged with the mean/std values dataset, to get one dataset with descriptive activity names

- Lastly, with the help of the "melt" and "dcast" functions of the "reshape2" package, the data is converted into a table containing mean values of all the included features, ordered by the activity name and the subject id, and the data is written to the "tidy_movement_data.txt" file.


### Additional Information
You can find additional information about the variables, data and transformations in the CodeBook.MD file.