# Facial_Recognition
Steps:

1)  Detect Face from the Image: We get an array of bounding box of human face by using different models for detecting faces.
­   Various models that can be used:
             i) HOG (Histogram of Oriented Gradients) 
                 -Less accurate but faster on CPU’s.
                 -More accurate than Haar cascades
             ii) Haar Cascades
                 -Fast but less accurate
             iii) Deep Learning based detector ( CNN based detector)
                 -More accurate than Haar and hog but can be very slow
                 -GPU can increase the speed

   We are using HOG for the face detection

2)  Detect the key Facial structure from the face ROI
    The pre-trained facial landmark detector is used to find 68 (x,y) coordinates on face.

              Then 128 dimension face encoding (measurements) are returned for the face using the
              68 specific points.
              How is it returning the measurements?
              A training set of labelled facial landmark for thousands of faces are taken and the model
              has been trained for several days using Deep convolutional network and hence it can 
              generate measurements for any face, even one it has never seen before.

3)  Comparing faces : compares 128 measurements for the known face and the unknown face infront of the webcam gives the prediction.


Procedure:

1) Run DataCollection.py for collecting facial data for any new user. It will first show the face that is going to be captured. If the face is not visible clearly press ctrl+c to exit otherwise press enter from the terminal. Then Enter the name.
If all goes fine the face will be shown in rectangular box

2) Run recognition.py for real time detection.

Results:

/home/vinit/Pictures/vin.png

