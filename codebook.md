---
title: "codebook.md"
author: "Prahlad"
date: "01/08/2019"
output: html_document
## R Markdown
Peer-Graded Assignment- Getting and Cleaning Data - Course Project V1.0

Created a script >>>"run_analysis.R"<<< to demonstrate the following:
 - Collection of Data
  -  Process the data
  - Clean the data set.
  
  Applied all variables and calculations  to generate the script >>>"run_analysis.R"<<< 
  
  Instruction 1. 
  Merge the training and the test sets to create one data set.
  1 Training data set file - "X_train.txt"
  2.Test data set file - "x_test.txt"
  
  The other files related data - i.e. activities and experiment subjects was also merged for better understanding the activities and the merged data set.
  
1.  All the follwing files were read using the read.table() and get data frame classes:
   a) x_train\test.txt
   b) y_train\test.txt
   c) subject_train\test.txt
   
2. cbind() function was used for merging training data set,activities and subject labels files corresponding to training data set.

3. test data set file was merged with activities and subjects lables file corresponding to test data set,once again using the cbind() function.

4. Dat frames in steps 2 and 3 above  were merged with rbind() function. The result was one data set - "data_set_variable". The data_set variable has first coulmn named "Subjects"  and second column named "Activities". All other ccolumns came from traaining and test data set named _______________

INSTRUCTION2

Extract only measurements on the mean and standard deviation for each measurement

a) read features.txt file by using read.table() function. This file has all the measurements e.g SD and mean.

b) To select rows with mean and SD  I used grep() function.

c) select() function was used to filter rows with the mean and SD measurements

d) A new data frame "extr_mean_std_data_set" with first two columns same as "data_set" and rest of the columns conatin the measurements for SD and mean.

INSTRUCTION 3

Use descriptive activity names to name the activities in the data set

a) "activity_labels.txt" file read using read.table() function

b) Changing values in second column of "extr_mean_std_data_set" use recode() and results written back to  "extr_mean_std_data_set"

INSTRUCTION 4
Appropriately labels the data set with descriptive variable names.

a) setnames() function used to change column names of related to mean measurments to descriptive variable names and result was saved as " extr_std_data_set"

b) old column names foe mean measurements was taken from " extr_std_data_set" and saved as "old_col_names_mean"
c) new column names for mean measurements was taken from "features_txt" and saved as "desc_col_names_mean"

d) Reapeat the above for col names related to std measurements.  "extr_mean_std_data" has been mutated to have a new descriptive ccolumn names  from 3rd to last column as required.

INSTRUCTION 5

From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

a)tidy data set created - average of each variable  for each subject - by working on the data set sorted accoring to subjects and activity values.

b) Tidy dta set with average of each variable for  each activity   created using for loop working on data set sorted accoring to subjects and activity values.

c) colMean() function to calculate mean for each column  in "sorted_data_set" corresponding to measurements

d)  Results saved to new data frame "second_data_set" with proper values for "Subjects" and "Activities" columns

e)  A second Independent tidy data set with average of each variable for each activity and each subject  using write.table() function with row.names = FALSE and saved as "tidy_data_set.txt"

