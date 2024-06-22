# A TinyML Object Detection Model
<br/> 

## 1. Introduction

## 2. Training Scripts
To Train, Validate and Test YOLOv5 models please refer to: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]()

To Train, Validate and Test YOLOv8 models please refer to: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]()

To Train, Validate and Test TFLite 2 models please refer to : [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]()

## 3. Deploy on rasberri-pi 

### 3.1 Pytorch models
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
# git clone https://github.com/lamao-ab/tinyml-object-detection-models.git
```

rename the folder to "wkspace" and then enter into it:

```
# mv tinyml-Object-Detection-models wkspace
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
# source wkspace-env/bin/activate
```

### yolov5
Install ultralytics pip package
```
# pip install ultralytics
# pip install tensorflow==2.13.1
# pip install -r requirements.txt 
```

Tap the command to clone to yolov5 repository:

```
# git clone https://github.com/
```
</details>

<details>
<summary>Run Inference </summary>
``` 
# cd yolov5
# python detect.py --data /home/pi/wkspace/demo/SOD-2/data.yaml --source /home/pi/wkspace/SOD-2/test/images/ --weights /home/pi/wkspace/demo/yolov5n.py  --imgsz 640 --conf 0.25
```
</details>


## yolov8
<details>
<summary>Run Inference </summary>
```
# pip install ultralytics==8.0.20
# pip install roboflow
# pip install --upgrade ultralytics
```
</details>

<details>
<summary>Run Inference </summary>

```
# cd yolov8
# yolo task=detect mode=predict source= /home/pi/wkspace/SOD-2/test/images/  model=/home/pi/wkspace/yolov8n.pt data=/home/pi/wkspace/SOD-2/data.yaml imgsz=640 conf=0.25 save=True 
```
</details>



### 3.1 TensorFlow Lite models
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
# git clone https://github.com/lamao-ab/tinyml-object-detection-models.git
```

rename the folder to "wkspace" and then enter into it:

```
# mv tinyml-Object-Detection-models wkspace
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


