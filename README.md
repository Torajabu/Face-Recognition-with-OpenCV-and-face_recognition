# Face-Recognition-with-OpenCV-and-face_recognition
![](https://github.com/Raj-med/Face-Recognition-with-OpenCV-and-face_recognition/blob/main/facerecog.gif)

This project demonstrates real-time face recognition using a webcam feed. The script leverages OpenCV for video processing and the `face_recognition` library for face detection and recognition.

## Requirements

- Python 3.x
- OpenCV
- face_recognition

### You can install the required libraries using pip:

pip install opencv-python face_recognition


## Setup
Clone this repository or download the script.

Ensure you have images of the known individuals you want to recognize. Place these images in a directory and update the file paths in the script accordingly.

Update the script with the file paths to your known face images and their corresponding names:
known_person1_image = face_recognition.load_image_file(r"path_to_your_image\person1.jpg")
known_person2_image = face_recognition.load_image_file(r"path_to_your_image\person2.jpg")
known_person3_image = face_recognition.load_image_file(r"path_to_your_image\person3.jpg")

# Replace with actual names
known_face_names.append("Person 1")
known_face_names.append("Person 2")
known_face_names.append("Person 3")

# Running the Script
Execute the script with Python:
python face_recognition.py


The script will access your webcam and start processing the video feed. It will attempt to recognize any faces in the frame and display a rectangle around detected faces along with their names.

Press the `q` key to exit the video feed and close the application.

## Script Explanation

### Imports and Initialization

- Import necessary libraries.
- Initialize lists to store known face encodings and names.

### Load Known Faces

- Load images of known individuals.
- Encode faces and store encodings and names in respective lists.

### Initialize Webcam

- Access the webcam using OpenCV.

### Process Video Frames

- Continuously capture frames from the webcam.
- Detect faces and compute face encodings for each face in the frame.
- Compare detected faces against known face encodings.
- Draw rectangles around faces and label them with names.

### Exit Conditions

- Display the processed frame.
- Exit when the `q` key is pressed.

## Notes

- Ensure your webcam is properly connected.
- The script uses the first face encoding found in each image. Make sure each image contains only one face for accurate encoding.
- Adjust the `r"path_to_your_image\..."` paths to reflect the actual paths to your image files.
- Also notice that eventhough the photo of me used in training was significatly different with full hair and no beard, the project successfully identifies me in the real time webcam with beard and shaven head
