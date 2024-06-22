# A TinyML Object Detection Model
<br/> 

## 1. Introduction

## 2. Training Scripts
To Train, Validate and Test YOLOv5 models please refer to: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]()

To Train, Validate and Test YOLOv8 models please refer to: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]()

To Train, Validate and Test TFLite 2 models please refer to : [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]()

## 3. Deploy on rasberri-pi 

<details>
<summary>Update the Raspberry Pi</summary>

On a termonal run the command to update the Raspberry Pi:
```
sudo apt-get update
sudo apt-get dist-upgrade
```

Then, enable the camera interface on raspberry-pi:
```
sudo raspi-config
```
Select the Interfaces tab and Enable the camera interface. and reboot the Raspberry Pi.

</details>

<details>
<summary>Download this repository and create virtual environment</summary>

Tap the command to clone this repository:

```
# git clone https://github.com/
```

rename the folder to "wkspace" and then cd into it:

```
# mv TensorFlow-Lite-Object-Detection-on-Android-and-Raspberry-Pi wkspace
# cd wkspace
```

Install virtualenv :

```
# sudo pip install virtualenv
```

Then, create and activate the "wkspace-env" virtual environment, which will contain all the package libraries for this environment:

```
# python -m venv wkspace-env
```
```
# source tflite1-env/bin/activate
```
</details>

<details>
<summary>Install TensorFlow Lite dependencies and OpenCV</summary>
  
```
# pip install tensorflow opencv-python protobuf==3.20.*
```
</details>

<details>
<summary>Run the TensorFlow Lite model</summary>
Run the real-time webcam detection script by executing the following command from inside the /home/pi/wkspace directory.
demo is a folder that contain the model file and label classes file. 
  
```
# python detection_webcam_voice.py --modeldir=demo
```
</details>

## 4. Low Light enhacement Module

## References


