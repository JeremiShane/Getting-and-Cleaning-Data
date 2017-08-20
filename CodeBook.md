# CodeBook


## Description of original data
>The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 
>
>The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 
>
> Note: Features are normalized and bounded within [-1,1].

## Description of the created data
1. Train and test of the above descibed data sets are combined
2. Columns with subjects and activities are added accordingly
4. Variables with means and standard deviations are preserved
4. A new tidy data set is created with a mean of each of these values for every subject and activity

The resulting data set has 180 rows and 68 columns. We have 30 subjects who each did 6 activities. For each of the combinations there are 66 different mean measurements. The columns are described below.

|	Column number| 	Column name	|	Description	|	Format	|	Domain	|	Reference point	|
|	----------------	|----------------	|	-------------	|	-------------	|	-------------	|	-------------	|
|		1 |SubjectID	|	ID of the subject taking part in the experiment	|	Numeric	|		|		|
|		2 |Activity	|	Activity that was carried out: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING	|	Character	|		|		|
|		3 |TimeBodyAccelerationMeanValueXdirection.Mean	|	The mean of the means of the body acceleration signal in the X-direction obtained by subtracting the gravity from the total acceleration (time domain)	|	Numeric	|	Time	|	Body	|
|		4 |TimeBodyAccelerationMeanValueYdirection.Mean	|	The mean of the means of the body acceleration signal in the Y-direction obtained by subtracting the gravity from the total acceleration (time domain)	|	Numeric	|	Time	|	Body	|
|		5 |TimeBodyAccelerationMeanValueZdirection.Mean	|	The mean of the means of the body acceleration signal in the Z-direction obtained by subtracting the gravity from the total acceleration (time domain)	|	Numeric	|	Time	|	Body	|
|		6 |TimeBodyAccelerationStandardDeviationXdirection.Mean	|	The mean of the standard deviations of the body acceleration signal in the X-direction obtained by subtracting the gravity from the total acceleration (time domain)	|	Numeric	|	Time	|	Body	|
|		7 |TimeBodyAccelerationStandardDeviationYdirection.Mean	|	The mean of the standard deviations of the body acceleration signal in the Y-direction obtained by subtracting the gravity from the total acceleration (time domain)	|	Numeric	|	Time	|	Body	|
|		8 |TimeBodyAccelerationStandardDeviationZdirection.Mean	|	The mean of the standard deviations of the body acceleration signal in the Z-direction obtained by subtracting the gravity from the total acceleration (time domain)	|	Numeric	|	Time	|	Body	|
|		9 |TimeGravityAccelerationMeanValueXdirection.Mean	|	The mean of the means of the the gravity acceleration in the X-direction (time domain)	|	Numeric	|	Time	|	Gravity	|
|		10 |TimeGravityAccelerationMeanValueYdirection.Mean	|	The mean of the means of the the gravity acceleration in the Y-direction (time domain)	|	Numeric	|	Time	|	Gravity	|
|		11 |TimeGravityAccelerationMeanValueZdirection.Mean	|	The mean of the means of the the gravity acceleration in the Z-direction (time domain)	|	Numeric	|	Time	|	Gravity	|
|		12 |TimeGravityAccelerationStandardDeviationXdirection.Mean	|	The mean of the standard deviations of the the gravity acceleration in the X-direction (time domain)	|	Numeric	|	Time	|	Gravity	|
|		13 |TimeGravityAccelerationStandardDeviationYdirection.Mean	|	The mean of the standard deviations of the the gravity acceleration in the Y-direction (time domain)	|	Numeric	|	Time	|	Gravity	|
|		14 |TimeGravityAccelerationStandardDeviationZdirection.Mean	|	The mean of the standard deviations of the the gravity acceleration in the Z-direction (time domain)	|	Numeric	|	Time	|	Gravity	|
|		15 |TimeBodyAccelerationJerkMeanValueXdirection.Mean	|	The mean of the means of the body jerk signal in the X-direction obtained by subtracting the gravity from the total jerk (time domain)	|	Numeric	|	Time	|	Body	|
|		16 |TimeBodyAccelerationJerkMeanValueYdirection.Mean	|	The mean of the means of the body jerk signal in the Y-direction obtained by subtracting the gravity from the total jerk (time domain)	|	Numeric	|	Time	|	Body	|
|		17 |TimeBodyAccelerationJerkMeanValueZdirection.Mean	|	The mean of the means of the body jerk signal in the Z-direction obtained by subtracting the gravity from the total jerk (time domain)	|	Numeric	|	Time	|	Body	|
|		18 |TimeBodyAccelerationJerkStandardDeviationXdirection.Mean	|	The mean of the standard deviations of the body jerk signal in the X-direction obtained by subtracting the gravity from the total jerk (time domain)	|	Numeric	|	Time	|	Body	|
|		19 |TimeBodyAccelerationJerkStandardDeviationYdirection.Mean	|	The mean of the standard deviations of the body jerk signal in the Y-direction obtained by subtracting the gravity from the total jerk (time domain)	|	Numeric	|	Time	|	Body	|
|		20 |TimeBodyAccelerationJerkStandardDeviationZdirection.Mean	|	The mean of the standard deviations of the body jerk signal in the Z-direction obtained by subtracting the gravity from the total jerk (time domain)	|	Numeric	|	Time	|	Body	|
|		21 |TimeBodyGyroscopeMeanValueXdirection.Mean	|	The mean of the means of the angular velocity in the X direction measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		22 |TimeBodyGyroscopeMeanValueYdirection.Mean	|	The mean of the means of the angular velocity in the Y direction measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		23 |TimeBodyGyroscopeMeanValueZdirection.Mean	|	The mean of the means of the angular velocity in the Z direction measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		24 |TimeBodyGyroscopeStandardDeviationXdirection.Mean	|	The mean of the standard deviations of the angular velocity in the X direction measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		25 |TimeBodyGyroscopeStandardDeviationYdirection.Mean	|	The mean of the standard deviations of the angular velocity in the Y direction measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		26 |TimeBodyGyroscopeStandardDeviationZdirection.Mean	|	The mean of the standard deviations of the angular velocity in the Z direction measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		27 |TimeBodyGyroscopeJerkMeanValueXdirection.Mean	|	The mean of the means of the jerk in the X direction measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		28 |TimeBodyGyroscopeJerkMeanValueYdirection.Mean	|	The mean of the means of the jerk in the Y direction measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		29 |TimeBodyGyroscopeJerkMeanValueZdirection.Mean	|	The mean of the means of the jerk in the Z direction measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		30 |TimeBodyGyroscopeJerkStandardDeviationXdirection.Mean	|	The mean of the standard deviations of the jerk in the X direction measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		31 |TimeBodyGyroscopeJerkStandardDeviationYdirection.Mean	|	The mean of the standard deviations of the jerk in the Y direction measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		32 |TimeBodyGyroscopeJerkStandardDeviationZdirection.Mean	|	The mean of the standard deviations of the jerk in the Z direction measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		33 |TimeBodyAccelerationMagnitudeMeanValue.Mean	|	The mean of the means of the magnitude of the body acceleration signal obtained by subtracting the gravity from the total acceleration (time domain)	|	Numeric	|	Time	|	Body	|
|		34 |TimeBodyAccelerationMagnitudeStandardDeviation.Mean	|	The mean of the standard deviation of the magnitude of the body acceleration signal obtained by subtracting the gravity from the total acceleration (time domain)	|	Numeric	|	Time	|	Body	|
|		35 |TimeGravityAccelerationMagnitudeMeanValue.Mean	|	The mean of the means of the magnitude of the gravity  (time domain)	|	Numeric	|	Time	|	Gravity	|
|		36 |TimeGravityAccelerationMagnitudeStandardDeviation.Mean	|	The mean of the standard deviations of the magnitude of the gravity  (time domain)	|	Numeric	|	Time	|	Gravity	|
|		37 |TimeBodyAccelerationJerkMagnitudeMeanValue.Mean	|	The mean of the means of the magnitude of the body jerk signal obtained by subtracting the gravity from the total jerk (time domain)	|	Numeric	|	Time	|	Body	|
|		38 |TimeBodyAccelerationJerkMagnitudeStandardDeviation.Mean	|	The mean of the standard deviation of the magnitude of the body jerk signal obtained by subtracting the gravity from the total jerk (time domain)	|	Numeric	|	Time	|	Body	|
|		39 |TimeBodyGyroscopeMagnitudeMeanValue.Mean	|	The mean of the means of the magnitude of the angular velocity vector measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		40 |TimeBodyGyroscopeMagnitudeStandardDeviation.Mean	|	The mean of the standard deviations of the magnitude of the angular velocity vector measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		41 |TimeBodyGyroscopeJerkMagnitudeMeanValue.Mean	|	The mean of the means of the jerk measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		42 |TimeBodyGyroscopeJerkMagnitudeStandardDeviation.Mean	|	The mean of the standard deviations of the magnitude of the jerk measured by the gyroscope for each window sample (time domain)	|	Numeric	|	Time	|	Body	|
|		43 |FrequencyBodyAccelerationMeanValueXdirection.Mean	|	The mean of the means of the body acceleration signal in the X-direction obtained by subtracting the gravity from the total acceleration (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		44 |FrequencyBodyAccelerationMeanValueYdirection.Mean	|	The mean of the means of the body acceleration signal in the Y-direction obtained by subtracting the gravity from the total acceleration (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		45 |FrequencyBodyAccelerationMeanValueZdirection.Mean	|	The mean of the means of the body acceleration signal in the Z-direction obtained by subtracting the gravity from the total acceleration (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		46 |FrequencyBodyAccelerationStandardDeviationXdirection.Mean	|	The mean of the standard deviations of the body acceleration signal in the X-direction obtained by subtracting the gravity from the total acceleration (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		47 |FrequencyBodyAccelerationStandardDeviationYdirection.Mean	|	The mean of the standard deviations of the body acceleration signal in the Y-direction obtained by subtracting the gravity from the total acceleration (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		48 |FrequencyBodyAccelerationStandardDeviationZdirection.Mean	|	The mean of the standard deviations of the body acceleration signal in the Z-direction obtained by subtracting the gravity from the total acceleration (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		49 |FrequencyBodyAccelerationJerkMeanValueXdirection.Mean	|	The mean of the means of the body jerk signal in the X-direction obtained by subtracting the gravity from the total jerk (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		50 |FrequencyBodyAccelerationJerkMeanValueYdirection.Mean	|	The mean of the means of the body jerk signal in the Y-direction obtained by subtracting the gravity from the total jerk (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		51 |FrequencyBodyAccelerationJerkMeanValueZdirection.Mean	|	The mean of the means of the body jerk signal in the Z-direction obtained by subtracting the gravity from the total jerk (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		52 |FrequencyBodyAccelerationJerkStandardDeviationXdirection.Mean	|	The mean of the standard deviations of the body jerk signal in the X-direction obtained by subtracting the gravity from the total jerk (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		53 |FrequencyBodyAccelerationJerkStandardDeviationYdirection.Mean	|	The mean of the standard deviations of the body jerk signal in the Y-direction obtained by subtracting the gravity from the total jerk (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		54 |FrequencyBodyAccelerationJerkStandardDeviationZdirection.Mean	|	The mean of the standard deviations of the body jerk signal in the Z-direction obtained by subtracting the gravity from the total jerk (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		55 |FrequencyBodyGyroscopeMeanValueXdirection.Mean	|	The mean of the means of the angular velocity in the X direction measured by the gyroscope for each window sample (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		56 |FrequencyBodyGyroscopeMeanValueYdirection.Mean	|	The mean of the means of the angular velocity in the Y direction measured by the gyroscope for each window sample (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		57 |FrequencyBodyGyroscopeMeanValueZdirection.Mean	|	The mean of the means of the angular velocity in the Z direction measured by the gyroscope for each window sample (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		58 |FrequencyBodyGyroscopeStandardDeviationXdirection.Mean	|	The mean of the standard deviations of the angular velocity in the X direction measured by the gyroscope for each window sample (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		59 |FrequencyBodyGyroscopeStandardDeviationYdirection.Mean	|	The mean of the standard deviations of the angular velocity in the Y direction measured by the gyroscope for each window sample (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		60 |FrequencyBodyGyroscopeStandardDeviationZdirection.Mean	|	The mean of the standard deviations of the angular velocity in the Z direction measured by the gyroscope for each window sample (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		61 |FrequencyBodyAccelerationMagnitudeMeanValue.Mean	|	The mean of the means of the magnitude of the body acceleration signal obtained by subtracting the gravity from the total acceleration (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		62 |FrequencyBodyAccelerationMagnitudeStandardDeviation.Mean	|	The mean of the standard deviation of the magnitude of the body acceleration signal obtained by subtracting the gravity from the total acceleration (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		63 |FrequencyBodyBodyAccelerationJerkMagnitudeMeanValue.Mean	|	The mean of the means of the magnitude of the body jerk signal obtained by subtracting the gravity from the total jerk (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		64 |FrequencyBodyBodyAccelerationJerkMagnitudeStandardDeviation.Mean	|	The mean of the standard deviation of the magnitude of the body jerk signal obtained by subtracting the gravity from the total jerk (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		65 |FrequencyBodyBodyGyroscopeMagnitudeMeanValue.Mean	|	The mean of the means of the magnitude of the angular velocity vector measured by the gyroscope for each window sample (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		66 |FrequencyBodyBodyGyroscopeMagnitudeStandardDeviation.Mean	|	The mean of the standard deviations of the magnitude of the angular velocity vector measured by the gyroscope for each window sample (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		67 |FrequencyBodyBodyGyroscopeJerkMagnitudeMeanValue.Mean	|	The mean of the means of the jerk measured by the gyroscope for each window sample (frequency domain)	|	Numeric	|	Frequency	|	Body	|
|		68 |FrequencyBodyBodyGyroscopeJerkMagnitudeStandardDeviation.Mean	|	The mean of the standard deviations of the magnitude of the jerk measured by the gyroscope for each window sample (frequency domain)	|	Numeric	|	Frequency	|	Body	|


# Licence
Use of this dataset in publications must be acknowledged by referencing the following publication [1] 

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.

Jorge L. Reyes-Ortiz, Alessandro Ghio, Luca Oneto, Davide Anguita. November 2012.
