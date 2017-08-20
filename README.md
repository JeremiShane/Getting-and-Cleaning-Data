# Getting and Cleaning Data Course Project

## Introduction
The collections of files in this repository are the submission to the final assignment of 'Getting and Cleaning Data' by Olga Hartoog, created on 20-08-2017.

## Contents
1. README.md (this file)
2. CodeBook.md
3. run_analysis.R
4. tidydata.txt

## Original assignment

> ### Getting and Cleaning Data Course Project
> The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. 
> You will be required to submit: 
>
>1) a tidy data set as described below, 
>
>2) a link to a Github repository with your script for performing the analysis, and >
>3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. 
>
>You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.
>
> One of the most exciting areas in all of data science right now is wearable computing - see for example this article . Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained:
>
> http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 
>
> Here are the data for the project:
>
> https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 
> 
> You should create one R script called run_analysis.R that does the following.
>
> 1. Merges the training and the test sets to create one data set.
>
> 2. Extracts only the measurements on the mean and standard deviation for each measurement. 
> 
> 3. Uses descriptive activity names to name the activities in the data set
> 
> 4. Appropriately labels the data set with descriptive variable names. 
> 
> 5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
>
>
> Good luck!

## Description of files

### 1. README.md
The purpose of this file is to explain the analysis files in a clear and understandable way. Furthermore, a detailed description of the steps in the program is provided.

### 2. CodeBook.md
The CodeBook provides an explanation of the resulting data and a short description of how this results from the source data. 

### 3. run_analysis.R
This program runs the described tidying process of the data. 

In order to run this piece of code, clone this repository by the following commanf in your terminal
```
git clone https://github.com/ohartoog/Getting-and-Cleaning-Data.git
```
Run the code in Rstudio with 
```R
source("run_analysis.R")
```
or directly from the command line

### 4. tidydata.txt
This is the ouput of step 5 in the assignment. It is best viewed by reading in in back to R with the following command
```R
data <- read.table("tidydata.txt", header = TRUE)
```
### Steps in the creation of the tidy data set
Explanation of the code and choices that were made

#### 1. Dowloading and reading the data
The data are downloaded unless already present

```R
tmp <- tempfile()
if(!file.exists('./data/UCI HAR Dataset')) {
  download.file("https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip",tmp)
  unzip(tmp,exdir = './data')
}
```
The data are read in, for instance:
```R
activity_labels <- read.table(file="./data/UCI HAR Dataset/activity_labels.txt", sep = "",header = F)
```
The following data sets are read in:

* **x_train**: measurements of the training set

* **x_test**: measurements of the test set

* **y_train**: activity IDs of the train set, assumed to be in the same row order as the x_train

* **y_test**: activity IDs of the test set, assumed to be in the same row order as the x_test

* **subject_train**: subjects IDs of the train set, assumed to be in the same row order as the x_train

* **subject_test**: subjects IDs of the test set, assumed to be in the same row order as the x_test

* **features**: all features, assumed to be in the same column order as the x_* files

* **activity_labels**, a translation between and activity_id and an activity name


#### 2. Appropriately labeling the data set with descriptive variable names 
Names of the features are extracted, and a more descriptive version is produced (for the ones that we will use in the end)
```R
features_vector <- as.vector(features$V2)

features_vector_descriptive <- gsub("^t","Time",features_vector)
features_vector_descriptive <- gsub("^f","Frequency",features_vector_descriptive)
features_vector_descriptive <- gsub("BodyAcc","BodyAcceleration",features_vector_descriptive)
features_vector_descriptive <- gsub("GravAcc","GravityAcceleration",features_vector_descriptive)
features_vector_descriptive <- gsub("GravityAcc","GravityAcceleration",features_vector_descriptive)
features_vector_descriptive <- gsub("BodyBody","Body",features_vector_descriptive)
features_vector_descriptive <- gsub("Gyro","Gyroscope",features_vector_descriptive)
features_vector_descriptive <- gsub("Mag","Magnitude",features_vector_descriptive)
features_vector_descriptive <- gsub("-mean\\(\\)","MeanValue",features_vector_descriptive)
features_vector_descriptive <- gsub("-std\\(\\)","StandardDeviation",features_vector_descriptive)
features_vector_descriptive <- gsub("-X","Xdirection",features_vector_descriptive)
features_vector_descriptive <- gsub("-Y","Ydirection",features_vector_descriptive)
features_vector_descriptive <- gsub("-Z","Zdirection",features_vector_descriptive)
```
The (partly) descriptive column names are applied to the measurements sets
```R
colnames(x_train) <- features_vector_descriptive
colnames(x_test)  <- features_vector_descriptive
```
Descriptive column names are also added to the other tables. Colums that will be used to merge on later are given the same name
```R
colnames(activity_labels)   <- c("activity_label","Activity")
colnames(y_train)           <- c("activity_label")
colnames(y_test)            <- c("activity_label")
colnames(subject_train)     <- c("SubjectID")
colnames(subject_test)      <- c("SubjectID")
```

#### 2.  Extracting only the measurements on the mean and standard deviation for each measurement. 
Columns that have "-mean()" or "-std()" in their original name are taken into account. The rest is discarded from the x_* sets

```R
a <- grep("-mean\\(\\)",features_vector)
b <- grep("-std\\(\\)",features_vector)
c <- sort(unique(union(a,b)))
x_train <- x_train[,c]
x_test  <- x_test[,c]
```
Note: It could be debated that other variables should be included in the means and standard deviations. The assignment is ambiguous about that. 

#### 3. Using descriptive activity names to name the activities in the data set
The activity IDs and subject IDs are added to the test and train sets, and activity discriptions are added with merge(). 

Note: Merge() reorders data frames, but since we have already added all information, this is not a problem.
```R
data_train <- cbind(subject_train,y_train,x_train)
data_train <- merge(data_train,activity_labels)
```
#### 4. Adding a column to identify the origin of the data and reorder the reusult

Finally, with the select() function from the 'dplyr' package, we reorder the columns and discard the activity ID.
```R
data_train_select <- select(data_train,SubjectID,Group,Activity,3:69)
```
Step 3 and 4 are carried out with the group of test set data frames in a similar fashion.

#### 5. Merge the training and the test sets to create one data set 
Then the train and test data sets, that have exactly the same columns, are combined with rbind()

```R
data_tidy <- rbind(data_train_select,data_test_select)
```
Note: The assignment states to start with this step. Doing this would have involved fewer steps. However, I wanted to be sure that the orders would not mix up, such that the activities and subject IDs would not make sense. 

The resulting data set is tidy:

* one row is one observation

* each variable has its own column

* variable names are descriptive


#### 6. From the data set in step 4, creation of a second, independent tidy data set with the average of each variable for each activity and each subject.

The group_by() function from the package 'dplyr' is used to identify what are the columns that are not to be averaged, but stay as columns in the result
```R
data_groups           <- group_by(data_tidy,SubjectID,Activity)
```
Now the means of the remaining columns are calculated. 
```R
data_means            <- summarize_all(data_groups,mean,na.rm = TRUE)
```
We create new column names by adding the postfix ".Mean" to the existing ones
```R
columns               <- names(data_groups)[-(1:2)]
newcolumns            <- paste(columns,".Mean",sep='')
colnames(data_means)  <- union(colnames(data_means)[1:2],newcolumns)

```
The new data set is exported
```R
write.table(data_means,"tidydata.txt")
```


