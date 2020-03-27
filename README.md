# Drowsiness-Detection-System-for-Drivers
Driver drowsiness detection is a car safety Technology which helps prevent accidents caused by the driver getting drowsy. The following code uses computer vision to observe the driver's face, either using a built-in camera or on mobile devices. It is responsible for 72,000 crashes, 44,000 injuries, and 800 deaths annually in the US. When driver fatigue or drowsiness is detected, the system alerts the driver to prevent possible accidents. 

# Work-Flow
If a face is found, we apply facial landmark detection and extract the eye regions. Now that we have the eye regions, we can compute the eye aspect ratio (detailed here) to determine if the eyes are closed. f the eye aspect ratio indicates that the eyes have been closed for a sufficiently long enough amount of time, we’ll sound an alarm to wake up the driver.

## Algorithm
The algorithm is based on calculating an eye aspect ratio(EAR) which I will explain further. Each eye is represented by 6 (x, y)-coordinates, starting at the left-corner of the eye (as if you were looking at the person), and then working clockwise around the eye:

<img src="https://github.com/muskanvk/Drowsiness-Detection-System-for-Drivers/blob/master/eye1.jpg">

##Conditions and Relationships
Python’s dlib library uses Kazemi and Sullivan’s One Millisecond Face Alignment with an Ensemble of Regression Trees to implement the eye blink feature on the face.The program uses a facial training set to understand where certain points exist on facial structures. The program then plots the same points on region of interests in other images, if they exists. The program uses priors to estimate the probable distance between keypoints.





It checks 20 consecutive frames and if the Eye Aspect ratio is less than 0.25, Alert is generated. Eye aspect Ratio is calculated by the given formula.
