**Object Detection AI with ml5.js and COCO-SSD**


This JavaScript code creates a web application for object detection, utilizing the **ml5.js library** to identify objects in real-time from the video stream. **ml5.js** provides a simple API to run machine learning models directly in the browser, and the project uses the **COCO-SSD (Convolutional Object Classifier)** model for object detection.


**FEATURES**

**1. CAMERA ACCESS & VIDEO STREAM**


The application uses the navigator.mediaDevices.getUserMedia(constraints) function to access the user's camera and streams the video to an HTML video element. The camera can be set to use the back camera (e.g., on mobile devices) by specifying the facingMode: "environment" option.

**2. LOADING THE MODAL**


![object_detection_ai1](https://github.com/user-attachments/assets/44123307-b6bf-4a22-a597-7f1282d7c4c4)


This line loads the **COCO-SSD** model, which detects objects in the video stream, identifying their types and positions within the frame. The modelLoaded() function is triggered once the model is successfully loaded, updating the modelIsLoaded variable to true.


**3. ENABLING AI DETECTION**


Users can toggle AI detection on or off via a switch button. When enabled, the objects in the video stream are detected using the objectDetector.detect(c1, (err, results) => {...}) function.


**4. FPS (Frames Per Second) CONTROL**

Users can adjust the FPS (frames per second) using a range input. The changeFps() function updates the FPS based on the user's selection, allowing more or fewer frames to be processed per second.


**5. OBJECT DETECTION & RENDERING **

![object_detection_ai2](https://github.com/user-attachments/assets/e0d7dec2-0c46-44fe-a346-53c70639c0ed)


This function detects objects in each frame of the video feed and returns them in the results array. Each object includes properties such as position (x, y, width, height), label (label), and confidence score (confidence).



**LIBRARIES USED**

**ml5.js** : This library enables object detection in the browser using machine learning models, including the COCO-SSD model.

**COCO-SSD Model** :A pre-trained object detection model capable of recognizing around 80 object classes.

