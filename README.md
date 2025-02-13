# Getting-and-Cleaning-Data
The course project for the Getting and Cleaning Data Coursera course
____________________________________________________________________
Steps for arriving at the final tidy data set:
1)Read in the names of the components of the feature vectors from the file features.txt in the folder "UCI HAR Dataset" and cconvert it to a character vector.
2)Read in the data frame with the features vectors for the test and train data sets. Concatenate the two data frames row-wise into a single data frame and assign the names read from step (1) to the column names of this new data frame which has the feature vectors from the entire experiment.
3)Read in the activity codes for the experiment for the test and train data sets. Concatenate them into a single data frame row-wise. Now, read in the file with activity codes matched to the descriptions of the activities. Using this, create a data frame with a single column giving the activity description corresponding to each feature vector in the experiment as given by the data frame from step (2). This column has been assigned the name ActivityDescription.
4)Read in the subject codes for the test and train data sets and concatenate them row-wise into a single data frame. The single column in this data frame is named "Subject".
5)Now, concatenate the data frames from steps (4), (3) & (2) (in that order) column-wise into a single data frame.
6)Determine which columns correspond to calculations of mean using the function mean() and standard deviation using the function std().
7)Modify the data frame from step (5) and retain only the columns of interest determined in step (6).
8)For the data frame from step (7), rename the variables(column names) to make them more descriptive.
9)Group the data frame from step (8) by subject code and activity description.
10) For each pair of subject code and activity description, calculate the mean values for the other columns and create a new data set with the subject code, activity description and the calculated mean values for the other variables. This is the tidy data set we are interested in.
11)Write the tidy data set from step (10) to the text file "tidy_data.txt".

Read the tidy data file with the command:
read.table("tidy_data.txt", header=TRUE)




