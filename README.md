# Dozy-Detector
System that can automatically detect driver doziness in a real-time video stream and then play an alarm if the driver appears to be dozy.

## The dozy detector algorithm
The general flow of our dozy detection algorithm is fairly straightforward.

* First, camera will be setup that monitors a stream for faces.
* If a face is found,facial landmark detection will be aplied in order to extract the eye regions.
* Now that we have the eye regions, we can compute the eye aspect ratio to determine if the eyes are closed or not.
* If the eye aspect ratio indicates that the eyes have been closed for a sufficiently long enough amount of time, we’ll sound an alarm to wake up the driver.

## Testing the OpenCV doziness detector
python dozy.py \--shape-predictor shape_predictor_68_face_landmarks.dat \--alarm alarm.wav
