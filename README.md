---
title: "Readme.md"
author: "Prahlad"
date: "01/08/2019"
output: html_document
---
## R Markdown
## Peer  Graded Assignment : Getting and Cleaning Data Project Verion1.0
Features Realized and Results:

Instructions - Project Objectives:

1. Merge the Training and Test sets to create one tidy data set

2. Extract only the  measurements on the mean and standard deviation for each measurement.

3. Use Descriptive activity names to name the activities in the data set.

4. Appropriately Label the data set with descriptive variable names.

5. from the data sets in above step (step no 4), create a second, independent tidy data set with thr average of each variable for each activity and each subject.

These objectives are achieved by the scropt file >>>"run_analysis.R"<<<

Further details related to the above are given in  file >>>>"codebook.md"<<<

Final Resultss from the 5th instruction above is given in >>>"tidy_data-set.txt"<<< using the function write.table(). This also contains the argument row.names = FALSE

Summary of Delivered Files

1. "README.md" - this file should gives the activity plan and should be read first.

2. "run_analysis.R"- R script file. This processes the data as per the Coursera Project Assignment - "Peer Graded Assignment - Getting and Cleaning Data"
3. "codebook.md" - The file describes the 
     - Variables
     - the data
     - Transformation or work performed to cleanup the data
     
4. Tidy Data set, Activities Description, Mean nad Std deviation as caluclated are in the relevant files.
      



