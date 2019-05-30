
# Indoor/Outdoor Security System

Goal of this project is deployment of security system for detection of human for indoor/outdoor. 

The final product is an embedded system equipped with camera that in real-time gives alarm in the case of seeing human. 
This project has two main steps: 
In the first step, I implemented the YOLOv3 object detection which is finetuned for new dataset.
In the second step, I deploy the inference part on embedded system (Dragon board 410C) using C++ to 
have real-time performance. 



# 1.Training 

## Dataset


## Backbone Network




## Number of Prior Boxes



## MultiBox Detection



## Hard Negative Mining (HNM)


## Image Augmentation



## Loss function




## Fine-tuning





# 2.Deployment on DragonBoard 410c
To deploy YOLOv3 object detection on the DragonBoard 410c, I did/prepared the following steps:


### Hardware requirements:
- Using a DragonBoard 410c, USB camera, keyboard, mouse, HDMI monitor.
- Using a 16GB MicroSD Card
- Partition the 16GB MicroSD card into 4GB and 12GB.
- The 4GB of SD card was used to increase the memory (DragonBoard 410c has 1GB memory).
- The 12GB of SD card was used to increase the storage (DragonBoard 410c has 8GB storage).


### Software requirements:
- Installation of Debian linux
- Installation of Bazel (to compile tensorflow)
- Installation of Tensorflow 
- Installation of OpenCV
- The object detection code


### Pipeline of our system for pedestrain detection
The pipeline of our system includes the following steps:

- Capture the live video from camera 
- Extract the images/frames from the input video 
- Resize every image/frame for the YOLOv3 network
- Run the YOLOv3 network on the resized image/frame
- Apply the Non-Maximum Suppression algorithm to get rid of multiple detections of a single object
- Display the frames with the bounding box of detected objects.















 
