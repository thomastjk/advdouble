# AdvDouble
![example](https://github.com/thomastjk/advdouble/blob/main/eg1.png)

Real-time object detection is one of the key applications of deep neural networks (DNNs) for real-world mission-critical systems. While DNN-powered object detection systems celebrate many life-enriching opportunities, they also open doors for misuse and abuse. 

This project presents an adversarial patch attack on the YOLOv3 with Darknet53 detector. The pre-trained patch included in the Jupyter Notebook is trained with 1 epoch and has an attack success rate (ASR) of 80%. No further training was done beyond 1 epoch since it took over 14 hours. The ASR can be further increased with more training. This can be carried on by the next user.

# Trial 16x16 Inconspicuous Patch

I tried to generate a 16x16 patch with the goal of inconspicuity in mind. However, the results were not ideal. ASR achieved was below 2%.

The 16x16 patch is shown below:

![example](https://github.com/thomastjk/advdouble/blob/main/16x16.png)

The 16x16 patch in action. In this instance, it works. 

![example](https://github.com/thomastjk/advdouble/blob/main/16x16%20vanishing.png)

But not in this instance, which is the majority of the case:

![example](https://github.com/thomastjk/advdouble/blob/main/16x16%20no%20vanishing.png)

# Working Pretrained Patches

Below are the double patches generated with an ASR of 80%. 

This is the 26x26 pixel patch generated to be placed on the right cheek 

![example](https://github.com/thomastjk/advdouble/blob/main/cheekpatch.png)

This is the 26x26 pixel patch generated to be placed on the forehead

![example](https://github.com/thomastjk/advdouble/blob/main/forehead%20patch.png)

To use the pretrained patch, please run the cell marked with the title "Pretrained Patch". It can be found in the lower sections of the Jupyter Notebook named "Double TOG".

# Installation and Dependencies 
This project runs on Python 3.6. You are highly recommended to create a virtual environment to make sure the dependencies do not interfere with your current programming environment. By default, GPUs will be used to accelerate the process of adversarial attacks.

To install related packages, run the following command in terminal:
```
pip install -r requirements.txt
```

This attack also uses the [face_recognition](https://github.com/ageitgey/face_recognition) package. To install it , run the following command:
``` 
!pip install face_recognition
```

To be able to initialize the YOLOv3 model, please download the pretrained weights below!

[Link to YOLOv3 weights](https://www.dropbox.com/s/rx3r15fg8h1jl8v/YOLOv3_Darknet53.h5?dl=0)

# Instruction

The Jupyter Notebook named "Double TOG" is used to demonstrate the adversarial effects of the double patch generated. 

# Results 

After generating the double patch, several basic adversarial defense methods were used in the evaluation of the patches' spatial robustness. Basic affine transformations like scaling, rotating and translating were employed. Below are the graphs showing the effect of the affine transformation on the patches' ASR. 

Effects of Rotation on ASR:

![example](https://github.com/thomastjk/advdouble/blob/main/asr%20vs%20rotation.png)

Effects of Scale on ASR:

![example](https://github.com/thomastjk/advdouble/blob/main/asr%20vs%20scale.png)

Effects of no. of pixels shift in ASR: (Positive is rightwards and downwards)

![example](https://github.com/thomastjk/advdouble/blob/main/asr%20vs%20shift.png)

# Acknowledgement

This project was built upon the following project:

[TOG](https://github.com/git-disl/TOG)

[face_recognition](https://github.com/ageitgey/face_recognition)
