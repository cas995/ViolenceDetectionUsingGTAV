# ViolenceDetectionUsingGTAV
Violence Detection Using Grand Theft Auto V

# Deep learning framework
The proposed framework is based on the three-staged end- to-end framework of Ullah’s research [16]. The virtual gaming data is a new created dataset based on collected and self-created GTA-V videos. The deep learning framework will be divided into two parts: person identification and violence activity identification. The first part of the framework is to identify persons from the input surveillance videos. A MobileNet-SSD CNN model performs person identification. When a person is identified, the images are passed to a 3D CNN model. The second part of the framework is to identify violence scenarios using the 3D CNN model. This model is trained on virtual gaming data and extract spatiotemporal features. The spatiotemporal features are fed to the Softmax output layer of the 3D CNN model and predict whether or not there is a violent scene in the video. When a violent scenario is discovered, an alert could be sent to the nearest security department or a police station. A visual representation of the deep learning framework is shown in figure 1. 

![Alt text](DLFramework.png)
**Figure 1:**  Deep learning framework of the violent detection method.


## 1. Person identification
The incoming surveillance sequences were first assessed by a MobileNet-SSD CNN model [38]. This model was originally designed for object detection, fine-grain classification, face attributes and large-scale geolocation. In this thesis, this model was used for person identification. 

Open the folder /ViolenceDetectionUsingGTAV/MobilNet_SSD_opencv to see the code how people are identified in videos.

The file "/ViolenceDetectionUsingGTAV/MobilNet_SSD_opencv/RunModelOnVideo.ipynb" contains the main function for identifying people in videos.

The file offers two options:
1. You can upload an input video for the person identification model by yourself. As soon as a person is identified in the video, the video stops and the output prints that a person has been identified.
2. You can use your own camera. As soon as a person is identified on the image, a block is created around the person.

The script "/ViolenceDetectionUsingGTAV/MobilNet_SSD_opencv/RunModelOnVideo.ipynb", you can upload an input video for the person identification model. In this same script you can also choose to use your own camera. The camera then identifies people live in the recorded image.
## 2. Violence identification
