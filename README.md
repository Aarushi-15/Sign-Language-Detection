This project focuses on sign language recognition which will detect if the gesture is rock, paper or scissor. The following was the procedure followed.

<img width="308" alt="image" src="https://github.com/user-attachments/assets/44f10578-c5ea-4ff7-9f29-359fb27927bb">

### Creating Dataset 
OpenCV was used to get a live cam feed and read each frame. The first 60 frames taken to calculate the accumulated weight of the background so we can easily subtract this when the ROI contains some object.

![Screenshot (3)](https://github.com/user-attachments/assets/48a2e8a7-601f-4c03-80b7-faf472660636)

Background subtraction and findcontours function was used to see if any gesture was being portrayed. If any hand is detected, that particular frame or image is saved in a particular directory.

<img width="960" alt="Screenshot 2023-12-26 234537" src="https://github.com/user-attachments/assets/0b56dc69-3844-4e43-8e0b-11dad9dfa555">

Saving to directory when foreground object detected.

![Screenshot (4)](https://github.com/user-attachments/assets/930319e7-7130-4067-9512-21310115c8ef)

A total of 1806 images was created for the train and 108 images for the test categorised within 3 classes.
I used TensorFlow to build the model and use the flow_from_directory function of Keras to load our dataset.I defined a function to plot images along with their labels.
### Tranning
The necessary libraries were imported to design the Convolution Neural network. The model is then fitted amd tested on the testing batch.

<img width="960" alt="Screenshot 2024-01-02 090605" src="https://github.com/user-attachments/assets/b9e65cae-1c46-41d4-9fb9-5475be46a954">

### Prediting Gestures

<img width="524" alt="Screenshot 2024-01-02 092404" src="https://github.com/user-attachments/assets/eb371117-82c9-4cb2-8265-7758e74163df">

<img width="550" alt="Screenshot 2024-01-02 092445" src="https://github.com/user-attachments/assets/516b5199-ea95-4cf2-8a1d-c5c778ba6adb">

<img width="550" alt="Screenshot 2024-01-02 092445" src="https://github.com/user-attachments/assets/03d79845-f236-4186-a112-ea078daf2af9">









