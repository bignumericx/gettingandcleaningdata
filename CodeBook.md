---
title: "Human Activity Recognition Using Smartphones Dataset"
author: "Steeve Brechmann"
date: "Thursday, August 21, 2014"
output: html_document
---

<p><markdown>

##Dataset description

The data come from an experiment carried out with a group of 30 volunteers. 

Each person performed six activities:

 - Walking
 - Walking upstairs
 - Walking downstairs
 - Sitting
 - Standing
 - Laying

while wearing a smartphone on the waist. 

Using the embedded accelerometer and gyroscope, they captured the time valued 3-axial linear acceleration (tAcc-XYZ) and 3-axial angular velocity (tGyro-XYZ) at a constant rate of 50 Hz.

The acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ).

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). 

Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag.

## Variables description

We have the following description:

 - Subject_ID: subject unique identifier
 - Activity: activity name
 - BodyAcc: body acceleration signal
 - GravityAcc: gravity acceleration signal
 - BodyAccJerk: jerk body acceleration signal
 - BodyGyro: body gyroscopic signal
 - BodyGyroJerk: jerk body gyroscopic signal
 - BodyAccMag: magnitude of the body acceleration signal
 - GravityAccMag: magnitude of the gravity acceleration signal
 - BodyAccJerkMag: magnitude of the jerk body acceleration signal
 - BodyGyroMag: magnitude of the body gyroscopic signal
 - BodyGyroJerkMag: magnitude of the jerk body gyroscopic signal

From these, we obtain:

 - [t|f]BodyAcc-[X|Y|Z]
 - [t|f]GravityAcc-[X|Y|Z]
 - [t|f]BodyAccJerk-[X|Y|Z]
 - [t|f]BodyGyro-[X|Y|Z]
 - [t|f]BodyGyroJerk-[X|Y|Z]
 - [t|f]BodyAccMag
 - [t|f]GravityAccMag
 - [t|f]BodyAccJerkMag
 - [t|f]BodyGyroMag
 - [t|f]BodyGyroJerkMag

Where we use the [t|f]BodyAcc-[X|Y|Z] notation to represent the time (frequency) valued body acceleration signal in the X (Y or Z) direction.

For each of these 33 features, we take the mean and standard deviation. Hence, we have a total of 66 features.

## Transformation

Each transformations made on the raw data are explained in the comments of the run_analysis.R script. 

## Notes

 1. *Jerk* is the time rate of change of acceleration.
 2. Each variables are normalized and bounded within [-1, 1].
 3. Each variables vector is a row in the text file.
 4. The tidy dataset is a 180-by-68 data frame.


</markdown></p>