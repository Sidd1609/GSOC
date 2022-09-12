<div align="center">
    <a href="https://summerofcode.withgoogle.com/"><img src="https://godotengine.org/storage/app/uploads/public/5c7/67d/8c6/5c767d8c62621713488685.png" width="550" alt="google-summer-of-code"></a>
    <br>
    <b> 
    <p>
    Adding support of Source Code Related Metrics to OpenCV Zoo for <a href="https://github.com/opencv/opencv_zoo">OPENCV</a> Project
    </p>
    </b>
</div>
<p align="center">
    <code> 
	<a href="#-Project-Abstract">Project Abstract</a>&nbsp;&nbsp;&nbsp;
    	<a href="#-Contributions">Contributions</a>&nbsp;&nbsp;&nbsp;
    	<a href="#-Weekly-Summary">Weekly Summary</a>&nbsp;&nbsp;&nbsp;
	<a href="#-Would-like-to-sync">Would like to sync?</a>&nbsp;&nbsp;&nbsp;
    	<a href="#-Links">Links</a>
    </code>
</p>
<p align="center">
	<b> <sub>Check out my <a href="https://github.com/Sidd1609?tab=repositories"> <code>GitHub Repo</code> </a> or follow me on <a href="https://www.linkedin.com/in/sri-siddarth-chakaravarthy-p-145675192/"> <code>LinkedIn</code> </a> </sub></b>
</p>
<br>

## # Project Abstract
```shell
Contributor: 'Sri Siddarth Chakaravarthy'
Mentor: 'Yuantao Feng'
Organisation: 'OpenCV'
Project: 'Light-weight Object Detection Models for Resource-Restricted Usage'
Coding-Period: 'June 13th - September 12th'
```

+ OpenCV is an open-source library developed mainly for real-time computer vision operations such as object detection, object tracking, etc. 
+ Currently, OpenCV supports trained models with benchmarked results on various datasets via its model_zoo. Some existing models include Yunet, Mobilenet, CRNN, etc. 
+ OpenCV zoo model library is mainly focused on providing developers with trained model weights in .ONNX format and quantized models (light-weight models) that can be used on CPU-only machines, their model library contain trained model weights that can be used for real-time inference on systems that do not have high computation power (no GPU). 
+ These models can also be directly deployed in applications and are quantized to int-8 versions using onnxruntime static_quantization module.

> <i> The aim of this project is to add object detection models such as Nanodet, EfficientDet, YOLOX, etc. to the list of existing models in the OpenCV model zoo  to enable model inference using OpenCV python package</i>

<br>

## # Work Product

> Demonstration of object detection models updated to OpenCV Zoo models library: 
> <i> The final deliverable of this GSOC program was to help opencv_zoo support more light-weight object detection models so that developers will be able to infer models using <b>cv.dnn</b> framework, providing an alternative to existing model inference tools such as onnxruntime, openvino, tensorflow, etc. Towards the final timeline of this project we finalized models: NanoDet and YOLOX and have successfully added these model supports to opencv zoo library. </i>
<br>
Here are some of the <b>cv.dnn</b> inference observed when testing ONNX formatted models on a CPU-only machine. 

<div>
<p align="centre">
  <img src="https://github.com/Sidd1609/opencv_zoo/blob/master/models/object_detection_nanodet/examples/results/WebCamR.gif" width="450" height="450"> 
  <img src="https://github.com/Sidd1609/opencv_zoo/blob/master/models/object_detection_yolox/examples/results/WebcamR.gif" width="450" height="450">
</p>
</div>

## # Contributions
**#** **Repository: opencv_zoo** [**`/working-branches`**](https://github.com/opencv/opencv_zoo/branches)

<b> Pull requests created: </b>

1. [opencv/opencv_zoo#75](https://github.com/opencv/opencv_zoo/pull/75): [opencv_zoo] Added NanodetPlus model to the OpenCV Zoo models stack **`/cp1`**

2. [opencv/opencv_zoo#86](https://github.com/opencv/opencv_zoo/pull/86): [opencv_zoo] Added YOLOX model to the OpenCV Zoo models stack **`/cp2`**

3. [opencv/opencv_zoo#91](https://github.com/opencv/opencv_zoo/pull/91): [opencv_zoo] Added COCO_Evaluation support in OpenCV Zoo tools **`/cp3`**

<b> Issues opened: </b>
1. [opencv/opencv_zoo#62](https://github.com/opencv/opencv_zoo/issues/62#-weekly-summary ): [opencv_zoo] This issue directs to this page which consists of the detailed information about this project and all the contributions made by myself during the course of GSOC'22 **`/cb`**

2. [Megvii-BaseDetection/YOLOX#1464](https://github.com/Megvii-BaseDetection/YOLOX/issues/1464): [YOLOX] This issue was raised to inform an issue related to add CPU evaluation support for YOLOX so that it can be easier to infer models and run benchmarks on CPU only devices **`/cp1`**

> **Tags**:
>
> **c**ommunity **b**onding period : **`/cb`** <br>
> **c**oding **p**eriod **x** - **`/cpx`** <br>

<br>

## # Weekly Summary
### Community Bonding - May 20th to June 12th, 2022
<br>

### Coding Period 1 - June 13th to  July 25th, 2022

+ Week #1: [Summary](./Weekly_Logs/Week_1.md)
+ Week #2: [Summary](./Weekly_Logs/Week_2.md)
+ Week #3: [Summary](./Weekly_Logs/Week_3.md)
+ Week #4: [Summary](./Weekly_Logs/Week_4.md)
+ Week #5: [Summary](./Weekly_Logs/Week_5.md)
+ Week #6: <b> Sumission of Phase-1 Evaluation </b> [Summary](./Weekly_Logs/Week_6.md)

### Coding Period 2 - July 25th to  September 4th, 2022 

+ Week #7: [Summary](./Weekly_Logs/Week_7.md)
+ Week #8: [Summary](./Weekly_Logs/Week_8.md)
+ Week #9: [Summary](./Weekly_Logs/Week_9.md)
+ Week #10: [Summary](./Weekly_Logs/Week_10.md)
+ Week #11: [Summary](./Weekly_Logs/Week_11.md)

### Final Evaluation Period - September 5th to  September 12th, 2022

+ Week #12: <b> Sumission of Final Evaluation </b> [Summary](./Weekly_Logs/Week_12.md)
<br>

## # Would like to sync?

+ We have planned to keep all the communication open 🎉 so that everyone can sync and is free to participate and help us grow! So if you have suggestions/comments about anything please do not hesitate to open up an [issue ticket](https://github.com/opencv/opencv_zoo/issues)
<br>

## # Links

+ GSoC project [proposal](https://github.com/Sidd1609/GSOC/blob/main/SriSiddarth(OpenCV)(Proposal).pdf)
+ GSoC proposal [acceptance](https://summerofcode.withgoogle.com/programs/2022/projects/zULf6hi2)

<br>
