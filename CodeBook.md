#Human Activity Recognition Using Smartphones Dataset

#Dataset description

The data come from an experiment carried out with a group of 30 volunteers. 

Each person performed six activities:

 - Walking
 - Walking upstairs
 - Walking downstairs
 - Sitting
 - Standing
 - Laying

while wearing a smartphone on the waist. 

Using the embedded accelerometer and gyroscope, they captured the time valued 3-axial linear acceleration (tacc-xyz) and 3-axial angular velocity (tgyro-xyz) at a constant rate of 50 Hz.

The acceleration signal was then separated into body and gravity acceleration signals (tbodyacc-xyz and tgravityacc-xyz).

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain *jerk* signals (tbodyaccjerk-xyz and tbodygyrojerk-xyz). 

Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tbodyaccmag, tgravityaccmag, tbodyaccjerkmag, tbodygyromag, tbodygyrojerkmag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fbodyacc-xyz, fbodyaccjerk-xyz, fbodygyro-xyz, fbodyaccjerkmag, fbodygyromag, fbodygyrojerkmag.

## Variables description

The tidy data set contains the following variables:

 - subject_id: subject unique identifier
 - activity: activity name
 - bodyacc: body acceleration signal
 - gravityacc: gravity acceleration signal
 - bodyaccjerk: jerk body acceleration signal
 - bodygyro: body gyroscopic signal
 - bodygyrojerk: jerk body gyroscopic signal
 - bodyaccmag: magnitude of the body acceleration signal
 - gravityaccmag: magnitude of the gravity acceleration signal
 - bodyaccjerkmag: magnitude of the jerk body acceleration signal
 - bodygyromag: magnitude of the body gyroscopic signal
 - bodygyrojerkmag: magnitude of the jerk body gyroscopic signal

From these, we obtain:

 - subject_id
 - activity
 - [t|f]bodyacc_[mean|std]-[x|y|z]
 - [t|f]gravityacc_[mean|std]_[x|y|z]
 - [t|f]bodyaccjerk_[mean|std]_[x|y|z]
 - [t|f]bodygyro_[mean|std]_[x|y|z]
 - [t|f]bodygyrojerk_[mean|std]_[x|y|z]
 - [t|f]bodyaccmag_[mean|std]
 - [t|f]gravityaccmag_[mean|std]
 - [t|f]bodyaccjerkmag_[mean|std]
 - [t|f]bodygyromag_[mean|std]
 - [t|f]bodygyrojerkmag_[mean|std]

Where we use the [t|f]bodyacc_[mean|std]_[x|y|z] notation to represent the mean (standard deviation) value of the time (frequency) valued body acceleration signal in the x (y or z) direction.

By taking the mean and the standard deviation value of each signals, we obtain a total of 68 variables. 

## Transformation

 The transformations made on the variables names are:

 - Use lower case
 - Remove dots or white spaces

Subsequently, we take the average of each variable for each activity and each subject.

## Notes

 1. *Jerk* is the time rate of change of acceleration.
 2. Each variables are normalized and bounded within [-1, 1].
 3. Each variables vector is a row in the text file.
 4. The tidy dataset is a 180-by-68 data frame.