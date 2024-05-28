# Hand_Sign_detection
![Screenshot 2024-05-29 011436](https://github.com/sumitbehera1508/Hand_Sign_detection/assets/100491275/b97099f8-926e-43d9-9369-772506dcb742)


## PROBLEM STATEMENT      

As there are no readily available tools to assist individuals with no knowledge in sign language, a
significant communication gap persists when conversing with a deaf or mute person. This limitation
not only hinders effective communication but also perpetuates social barriers and isolation for
individuals with hearing or speech impairments.

By developing robust systems for real-time sign language recognition and translation, we can empower both deaf/mute individuals and their counterparts to engage in meaningful conversations and interactions, fostering inclusivity and accessibility in society.

## OBJECTIVE 

● Real-Time Detection: Implement a system capable of detecting hand signs in real-time from live video streams or recorded video footage.

● Accurate Hand Tracking: Utilize MediaPipe's hand tracking module to accurately detect and track hand landmarks, ensuring precise localization of hand gestures.

● Feature Extraction: Employ OpenCV techniques to extract relevant features from the detected hand landmarks, such as distances between key points and hand shape descriptors.

● Classification of Hand Signs: Develop and train machine learning models to classify the extracted features into predefined hand sign categories, enabling accurate recognition of sign language gestures.

## WORK FLOW
![WorkFLow](https://github.com/sumitbehera1508/Hand_Sign_detection/assets/100491275/ec6a61e5-8d44-49ea-8fdc-5e78822fe942)

## DATA SET

<p>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/0/0.jpg" alt="Hi" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/1/0.jpg" alt="A" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/2/0.jpg" alt="B" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/3/0.jpg" alt="C" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/4/0.jpg" alt="D" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/5/0.jpg" alt="E" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/6/0.jpg" alt="F" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/7/0.jpg" alt="G" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/8/0.jpg" alt="H" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/9/0.jpg" alt="I" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/10/0.jpg" alt="J" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/11/0.jpg" alt="k" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/12/0.jpg" alt="L" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/13/0.jpg" alt="M" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/14/0.jpg" alt="N" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/15/0.jpg" alt="O" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/16/0.jpg" alt="P" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/17/0.jpg" alt="Q" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/18/0.jpg" alt="R" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/19/0.jpg" alt="S" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/20/0.jpg" alt="T" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/21/0.jpg" alt="U" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/22/0.jpg" alt="V" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/23/0.jpg" alt="W" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/24/0.jpg" alt="X" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/25/0.jpg" alt="Y" width="150"/>
  <img src="https://github.com/sumitbehera1508/Hand_Sign_detection/blob/main/data1/26/0.jpg" alt="Z" width="150"/>
</p>

## DATA SET DESCRIPTION : 

![DATA COUNT](https://github.com/sumitbehera1508/Hand_Sign_detection/assets/100491275/4f9ea5a7-61dc-4058-8c5d-3d5755599b8e)
![Labels](https://github.com/sumitbehera1508/Hand_Sign_detection/assets/100491275/bd892666-4939-4408-ac02-01ed3591b378)

### A data set with 42 features is created according to the 21 key landmarks on the hand. The even indices show the X-coordinates while the odd indices show the Y-coordinates. Total 9741 images are used for the generation of the dataset. Two examples of generated data is given below :
![Real Data](https://github.com/sumitbehera1508/Hand_Sign_detection/assets/100491275/7ed67e27-3543-4a72-8741-9848210df399)

## DATA PROCESSING  :

● Create A list named “data_aux ” to store the processed landmark coordinates and two lists named “x_” and “ y_” to store the x and y coordinates of the hand landmarks.

● Captures a frame from the video source . Get the Height and width of the captured frame.

● Convert the frame from BGR (default color format in OpenCV) to RGB (required by MediaPipe).

● Processes the RGB frame to detect hand landmarks.

● If hand landmarks are detected, iterate through each hand and draw the landmarks and connections on the frame using MediaPipe's drawing utilities.

● For each detected hand, collect the normalized x and y coordinates of each landmark and store them in x_ and y_.

● For each landmark, adjust the coordinates by subtracting the minimum x and y values to normalize the position, and store them in data_aux.

### If the data is used during data set creation, the obtained data_aux list is stored in the data.picke file with the desired label then the next frame is processed. Otherwise, during classification the steps given below are followed :

● After data_aux list is created, Calculate the bounding box for the detected hand. Convert the normalized coordinates to pixel values and subtract 10 pixels for padding.

● Predict the hand sign using the model trained using the data.pickle file by passing the processed landmark data.

● Get the predicted character from the prediction result using a dictionary that maps the prediction output to characters.

● Draw a rectangle around the detected hand and display the predicted character above the bounding box.

## ScreenShots :

![Classification Report](https://github.com/sumitbehera1508/Hand_Sign_detection/assets/100491275/3648fd9f-c71d-4edb-880b-76cca0b4e60f)

### Confusion Matrix :
![Confusion Matrix](https://github.com/sumitbehera1508/Hand_Sign_detection/assets/100491275/46ba836d-61cc-4c57-adf8-01729558f320)

### Decesion Tree :
![decision_tree](https://github.com/sumitbehera1508/Hand_Sign_detection/assets/100491275/2596212e-07fc-4309-b8d3-e135a4011df0)


## OUTPUT :

https://github.com/sumitbehera1508/Hand_Sign_detection/assets/100491275/7200aa61-7053-473e-81e0-018bbd8be77a
