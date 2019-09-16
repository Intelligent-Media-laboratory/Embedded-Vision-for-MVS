# Intelligent Embedded Vision for Summarization of Multi-View Videos in IIoT

## Paper
https://ieeexplore.ieee.org/document/8815938



## How to Run? 
A step-wise tutorial explaining functionality of this code can be found here at links below (Part 1 and 2):
 - https://www.youtube.com/watch?v=SDq_5ZbTbqo
 - https://www.youtube.com/watch?v=aHvTtb8MbnQ

# Repository Explaination
There are total six Python script files and one two other folders [Models, suspicious-objects-detection] in this repository (Explained alphabetically).

### 1. complexity.py

It returns a single flot value which is used in "main_MVS_master_RPi.py" for summary generation.

### 2. encoding_decoding.py

This file has two functions where [encoding_image] takes input image and returns an encoded image and the function [decoding_image] function takes and decodes it into normal RGB format image.

### 3. entropy.py

It computes information inside image and returns a float value. It's input argument is image.

### 4. main_MVS_master_RPi.py

It receives frames for a certain duration from client RPis, decodes them and computes information by calling entropy and complexity functions and finally writes keyframes.

### 5. shots_segmentation_client_RPi.py

This code is executed over client RPis where a real-time video is captured, annotated, encoded and transmitted over WSN to master RPi.

### 6. yolo_main.py

This file takes input image and returns confidence scores and locations of detected objects.

## Models

Trained weights for tiny yolo can be downloaded from given link as follows:
- https://pjreddie.com/darknet/yolo/

## suspicious-objects-detection
======
For suspicious object detection we re-trained yolov3-tiny model for our own types of object detection i.e., suspicious objects that include gun, pistols, and knives. For annotating objects, first we downloaded different pictures from Google with several queries and take screenshots from some YouTube videos and movies. The overall training images were only 105 due to no public availability of such kind of dataset.




# Citation

If you are interested in Video Summarization domain you may find some of my other recent papers worthy to read:
<pre>
<code>
K. Muhammad, T. Hussain, and S. W. Baik, "Efficient CNN based summarization of surveillance videos for resource-constrained devices," Pattern Recognition Letters, 2018/08/07/ 2018

Hussain, Tanveer, Khan Muhammad, Amin Ullah, Zehong Cao, Sung Wook Baik, and Victor Hugo C. de Albuquerque. "Cloud-Assisted Multi-View Video Summarization using CNN and Bi-Directional LSTM." IEEE Transactions on Industrial Informatics (2019).
</code>
</pre>
