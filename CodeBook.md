# CodeBook


## Description of original data
>The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 
>
>The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 
>
> Note: Features are normalized and bounded within [-1,1].

## Description of the created columns

|	Column number| 	Column name	|	Description	|	Format	|	Domain	|	Reference point	|
|	----------------	|----------------	|	-------------	|	-------------	|	-------------	|	-------------	|
|		1 |"SubjectID"	|	ID of the subject taking part in the experiment	|	numeric	|		|		|
|		2 |"Activity"	|	Activity that was carried out: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING	|	character	|		|		|
|		3 |"TimeBodyAccelerationMeanValueXdirection_Mean"	|	The mean of the means of the body acceleration signal in the X-direction obtained by subtracting the gravity from the total acceleration (time domain)	|	numeric	|	Time	|	Body	|
|		4 |"TimeBodyAccelerationMeanValueYdirection_Mean"	|	The mean of the means of the body acceleration signal in the Y-direction obtained by subtracting the gravity from the total acceleration (time domain)	|	numeric	|	Time	|	Body	|
|		5 |"TimeBodyAccelerationMeanValueZdirection_Mean"	|	The mean of the means of the body acceleration signal in the Z-direction obtained by subtracting the gravity from the total acceleration (time domain)	|	numeric	|	Time	|	Body	|
|		6 |"TimeBodyAccelerationStandardDeviationXdirection_Mean"	|	The mean of the standard deviations of the body acceleration signal in the X-direction obtained by subtracting the gravity from the total acceleration (time domain)	|	numeric	|	Time	|	Body	|
|		7 |"TimeBodyAccelerationStandardDeviationYdirection_Mean"	|	The mean of the standard deviations of the body acceleration signal in the Y-direction obtained by subtracting the gravity from the total acceleration (time domain)	|	numeric	|	Time	|	Body	|
|		8 |"TimeBodyAccelerationStandardDeviationZdirection_Mean"	|	The mean of the standard deviations of the body acceleration signal in the Z-direction obtained by subtracting the gravity from the total acceleration (time domain)	|	numeric	|	Time	|	Body	|
|		9 |"TimeGravityAccelerationMeanValueXdirection_Mean"	|	The mean of the means of the the gravity acceleration in the X-direction (time domain)	|	numeric	|	Time	|	Gravity	|
|		10 |"TimeGravityAccelerationMeanValueYdirection_Mean"	|	The mean of the means of the the gravity acceleration in the Y-direction (time domain)	|	numeric	|	Time	|	Gravity	|
|		11 |"TimeGravityAccelerationMeanValueZdirection_Mean"	|	The mean of the means of the the gravity acceleration in the Z-direction (time domain)	|	numeric	|	Time	|	Gravity	|
|		12 |"TimeGravityAccelerationStandardDeviationXdirection_Mean"	|	The mean of the standard deviations of the the gravity acceleration in the X-direction (time domain)	|	numeric	|	Time	|	Gravity	|
|		13 |"TimeGravityAccelerationStandardDeviationYdirection_Mean"	|	The mean of the standard deviations of the the gravity acceleration in the Y-direction (time domain)	|	numeric	|	Time	|	Gravity	|
|		14 |"TimeGravityAccelerationStandardDeviationZdirection_Mean"	|	The mean of the standard deviations of the the gravity acceleration in the Z-direction (time domain)	|	numeric	|	Time	|	Gravity	|
|		15 |"TimeBodyAccelerationJerkMeanValueXdirection_Mean"	|	The mean of the means of the body jerk signal in the X-direction obtained by subtracting the gravity from the total jerk (time domain)	|	numeric	|	Time	|	Body	|
|		16 |"TimeBodyAccelerationJerkMeanValueYdirection_Mean"	|	The mean of the means of the body jerk signal in the Y-direction obtained by subtracting the gravity from the total jerk (time domain)	|	numeric	|	Time	|	Body	|
|		17 |"TimeBodyAccelerationJerkMeanValueZdirection_Mean"	|	The mean of the means of the body jerk signal in the Z-direction obtained by subtracting the gravity from the total jerk (time domain)	|	numeric	|	Time	|	Body	|
|		18 |"TimeBodyAccelerationJerkStandardDeviationXdirection_Mean"	|	The mean of the standard deviations of the body jerk signal in the X-direction obtained by subtracting the gravity from the total jerk (time domain)	|	numeric	|	Time	|	Body	|
|		19 |"TimeBodyAccelerationJerkStandardDeviationYdirection_Mean"	|	The mean of the standard deviations of the body jerk signal in the Y-direction obtained by subtracting the gravity from the total jerk (time domain)	|	numeric	|	Time	|	Body	|
|		20 |"TimeBodyAccelerationJerkStandardDeviationZdirection_Mean"	|	The mean of the standard deviations of the body jerk signal in the Z-direction obtained by subtracting the gravity from the total jerk (time domain)	|	numeric	|	Time	|	Body	|
|		21 |"TimeBodyGyroscopeMeanValueXdirection_Mean"	|	The mean of the means of the angular velocity in the X direction measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		22 |"TimeBodyGyroscopeMeanValueYdirection_Mean"	|	The mean of the means of the angular velocity in the Y direction measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		23 |"TimeBodyGyroscopeMeanValueZdirection_Mean"	|	The mean of the means of the angular velocity in the Z direction measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		24 |"TimeBodyGyroscopeStandardDeviationXdirection_Mean"	|	The mean of the standard deviations of the angular velocity in the X direction measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		25 |"TimeBodyGyroscopeStandardDeviationYdirection_Mean"	|	The mean of the standard deviations of the angular velocity in the Y direction measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		26 |"TimeBodyGyroscopeStandardDeviationZdirection_Mean"	|	The mean of the standard deviations of the angular velocity in the Z direction measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		27 |"TimeBodyGyroscopeJerkMeanValueXdirection_Mean"	|	The mean of the means of the jerk in the X direction measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		28 |"TimeBodyGyroscopeJerkMeanValueYdirection_Mean"	|	The mean of the means of the jerk in the Y direction measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		29 |"TimeBodyGyroscopeJerkMeanValueZdirection_Mean"	|	The mean of the means of the jerk in the Z direction measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		30 |"TimeBodyGyroscopeJerkStandardDeviationXdirection_Mean"	|	The mean of the standard deviations of the jerk in the X direction measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		31 |"TimeBodyGyroscopeJerkStandardDeviationYdirection_Mean"	|	The mean of the standard deviations of the jerk in the Y direction measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		32 |"TimeBodyGyroscopeJerkStandardDeviationZdirection_Mean"	|	The mean of the standard deviations of the jerk in the Z direction measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		33 |"TimeBodyAccelerationMagnitudeMeanValue_Mean"	|	The mean of the means of the magnitude of the body acceleration signal obtained by subtracting the gravity from the total acceleration (time domain)	|	numeric	|	Time	|	Body	|
|		34 |"TimeBodyAccelerationMagnitudeStandardDeviation_Mean"	|	The mean of the standard deviation of the magnitude of the body acceleration signal obtained by subtracting the gravity from the total acceleration (time domain)	|	numeric	|	Time	|	Body	|
|		35 |"TimeGravityAccelerationMagnitudeMeanValue_Mean"	|	The mean of the means of the magnitude of the gravity  (time domain)	|	numeric	|	Time	|	Gravity	|
|		36 |"TimeGravityAccelerationMagnitudeStandardDeviation_Mean"	|	The mean of the standard deviations of the magnitude of the gravity  (time domain)	|	numeric	|	Time	|	Gravity	|
|		37 |"TimeBodyAccelerationJerkMagnitudeMeanValue_Mean"	|	The mean of the means of the magnitude of the body jerk signal obtained by subtracting the gravity from the total jerk (time domain)	|	numeric	|	Time	|	Body	|
|		38 |"TimeBodyAccelerationJerkMagnitudeStandardDeviation_Mean"	|	The mean of the standard deviation of the magnitude of the body jerk signal obtained by subtracting the gravity from the total jerk (time domain)	|	numeric	|	Time	|	Body	|
|		39 |"TimeBodyGyroscopeMagnitudeMeanValue_Mean"	|	The mean of the means of the magnitude of the angular velocity vector measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		40 |"TimeBodyGyroscopeMagnitudeStandardDeviation_Mean"	|	The mean of the standard deviations of the magnitude of the angular velocity vector measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		41 |"TimeBodyGyroscopeJerkMagnitudeMeanValue_Mean"	|	The mean of the means of the jerk measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		42 |"TimeBodyGyroscopeJerkMagnitudeStandardDeviation_Mean"	|	The mean of the standard deviations of the magnitude of the jerk measured by the gyroscope for each window sample (time domain)	|	numeric	|	Time	|	Body	|
|		43 |"FrequencyBodyAccelerationMeanValueXdirection_Mean"	|	The mean of the means of the body acceleration signal in the X-direction obtained by subtracting the gravity from the total acceleration (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		44 |"FrequencyBodyAccelerationMeanValueYdirection_Mean"	|	The mean of the means of the body acceleration signal in the Y-direction obtained by subtracting the gravity from the total acceleration (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		45 |"FrequencyBodyAccelerationMeanValueZdirection_Mean"	|	The mean of the means of the body acceleration signal in the Z-direction obtained by subtracting the gravity from the total acceleration (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		46 |"FrequencyBodyAccelerationStandardDeviationXdirection_Mean"	|	The mean of the standard deviations of the body acceleration signal in the X-direction obtained by subtracting the gravity from the total acceleration (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		47 |"FrequencyBodyAccelerationStandardDeviationYdirection_Mean"	|	The mean of the standard deviations of the body acceleration signal in the Y-direction obtained by subtracting the gravity from the total acceleration (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		48 |"FrequencyBodyAccelerationStandardDeviationZdirection_Mean"	|	The mean of the standard deviations of the body acceleration signal in the Z-direction obtained by subtracting the gravity from the total acceleration (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		49 |"FrequencyBodyAccelerationJerkMeanValueXdirection_Mean"	|	The mean of the means of the body jerk signal in the X-direction obtained by subtracting the gravity from the total jerk (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		50 |"FrequencyBodyAccelerationJerkMeanValueYdirection_Mean"	|	The mean of the means of the body jerk signal in the Y-direction obtained by subtracting the gravity from the total jerk (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		51 |"FrequencyBodyAccelerationJerkMeanValueZdirection_Mean"	|	The mean of the means of the body jerk signal in the Z-direction obtained by subtracting the gravity from the total jerk (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		52 |"FrequencyBodyAccelerationJerkStandardDeviationXdirection_Mean"	|	The mean of the standard deviations of the body jerk signal in the X-direction obtained by subtracting the gravity from the total jerk (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		53 |"FrequencyBodyAccelerationJerkStandardDeviationYdirection_Mean"	|	The mean of the standard deviations of the body jerk signal in the Y-direction obtained by subtracting the gravity from the total jerk (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		54 |"FrequencyBodyAccelerationJerkStandardDeviationZdirection_Mean"	|	The mean of the standard deviations of the body jerk signal in the Z-direction obtained by subtracting the gravity from the total jerk (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		55 |"FrequencyBodyGyroscopeMeanValueXdirection_Mean"	|	The mean of the means of the angular velocity in the X direction measured by the gyroscope for each window sample (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		56 |"FrequencyBodyGyroscopeMeanValueYdirection_Mean"	|	The mean of the means of the angular velocity in the Y direction measured by the gyroscope for each window sample (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		57 |"FrequencyBodyGyroscopeMeanValueZdirection_Mean"	|	The mean of the means of the angular velocity in the Z direction measured by the gyroscope for each window sample (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		58 |"FrequencyBodyGyroscopeStandardDeviationXdirection_Mean"	|	The mean of the standard deviations of the angular velocity in the X direction measured by the gyroscope for each window sample (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		59 |"FrequencyBodyGyroscopeStandardDeviationYdirection_Mean"	|	The mean of the standard deviations of the angular velocity in the Y direction measured by the gyroscope for each window sample (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		60 |"FrequencyBodyGyroscopeStandardDeviationZdirection_Mean"	|	The mean of the standard deviations of the angular velocity in the Z direction measured by the gyroscope for each window sample (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		61 |"FrequencyBodyAccelerationMagnitudeMeanValue_Mean"	|	The mean of the means of the magnitude of the body acceleration signal obtained by subtracting the gravity from the total acceleration (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		62 |"FrequencyBodyAccelerationMagnitudeStandardDeviation_Mean"	|	The mean of the standard deviation of the magnitude of the body acceleration signal obtained by subtracting the gravity from the total acceleration (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		63 |"FrequencyBodyBodyAccelerationJerkMagnitudeMeanValue_Mean"	|	The mean of the means of the magnitude of the body jerk signal obtained by subtracting the gravity from the total jerk (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		64 |"FrequencyBodyBodyAccelerationJerkMagnitudeStandardDeviation_Mean"	|	The mean of the standard deviation of the magnitude of the body jerk signal obtained by subtracting the gravity from the total jerk (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		65 |"FrequencyBodyBodyGyroscopeMagnitudeMeanValue_Mean"	|	The mean of the means of the magnitude of the angular velocity vector measured by the gyroscope for each window sample (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		66 |"FrequencyBodyBodyGyroscopeMagnitudeStandardDeviation_Mean"	|	The mean of the standard deviations of the magnitude of the angular velocity vector measured by the gyroscope for each window sample (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		67 |"FrequencyBodyBodyGyroscopeJerkMagnitudeMeanValue_Mean"	|	The mean of the means of the jerk measured by the gyroscope for each window sample (frequency domain)	|	numeric	|	Frequency	|	Body	|
|		68 |"FrequencyBodyBodyGyroscopeJerkMagnitudeStandardDeviation_Mean"	|	The mean of the standard deviations of the magnitude of the jerk measured by the gyroscope for each window sample (frequency domain)	|	numeric	|	Frequency	|	Body	|


# Licence
Use of this dataset in publications must be acknowledged by referencing the following publication [1] 

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.

Jorge L. Reyes-Ortiz, Alessandro Ghio, Luca Oneto, Davide Anguita. November 2012.
