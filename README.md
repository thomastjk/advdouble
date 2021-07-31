# Introduction
![example](https://github.com/thomastjk/advdouble/blob/main/eg1.png)

Real-time object detection is one of the key applications of deep neural networks (DNNs) for real-world mission-critical systems. While DNN-powered object detection systems celebrate many life-enriching opportunities, they also open doors for misuse and abuse. 

This project presents an adversarial patch attack on the YOLOv3 with Darknet53 detector. The pre-trained patch included in the Jupyter Notebook is trained with 1 epoch and has an attack success rate (ASR) of 80%. No further training was done beyond 1 epoch since it took over 14 hours. The ASR can be further increased with more training. This can be carried on by the next user.

#Generated Patches 


# Installation and Dependencies 
This project runs on Python 3.6. You are highly recommended to create a virtual environment to make sure the dependencies do not interfere with your current programming environment. By default, GPUs will be used to accelerate the process of adversarial attacks.

To install related packages, run the following command in terminal:
```
pip install -r requirements.txt
```

This attack also uses the face_recognition package. To install it , run the following command:
``` 
!pip install face_recognition
```

To be able to initialize the YOLOv3 model, please download the pretrained weights below!

[Link to YOLOv3 weights](https://www.dropbox.com/s/rx3r15fg8h1jl8v/YOLOv3_Darknet53.h5?dl=0)

# Acknowledgement

This project was built upon the following project:

[TOG](https://github.com/git-disl/TOG)
