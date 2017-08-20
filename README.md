# Getting-and-Cleaning-Data

## Introduction
THe collections of files in front of you are the submission to the final assignment of 'Getting and Cleaning Data' by Olga Hartoog, created on 20-08-2017.

## Contents
1. README.md (this file)
2. CodeBook.md
3. run_analysis.R
4. tidydata.txt

## Original assignment

> ### Getting and Cleaning Data Course Project
> The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 1) a tidy data set as described below, 2) a link to a Github repository with your script for performing the analysis, and 3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.
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
> 1. Merges the training and the test sets to create one data set.
> 2. Extracts only the measurements on the mean and standard deviation for each measurement. 
> 3. Uses descriptive activity names to name the activities in the data set
> 4. Appropriately labels the data set with descriptive variable names. 
> 5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
>
> Good luck!

## 1. README.md
The purpose of this file is to explain the analysis files in a clear and understandable way. 

## 2. CodeBook.md
The CodeBook is intented to guide you through the code and provides an explanation of the resulting data and choices that have been made in the tidying process.

## 3. run_analysis.R
This program runs the described tidying process of the data. 

In order to run this, clone this repository by the following commang in your terminal
```
git clone https://github.com/ohartoog/Getting-and-Cleaning-Data.git
```

## 4. tidydata.txt
This is the ouput of step 5 in the assignment. It is best viewed by reading in in back to R with the following command
```
data <- read.table("tidydata.txt", header = TRUE) #if they used some other way of saving the file than a default write.table, this step will be differentView(data)
```
