This File is related to the Google Summer of Code 2022 for the proposal of Object detection models for OpenCV zoo carried out by Sri Siddarth Chakaravarthy 

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
    <a href="#-Pull-Requests,-Issues--Forks">Pull Requests & Issues</a>&nbsp;&nbsp;&nbsp;
    <a href="#-Weekly-Summary">Weekly Summary</a>&nbsp;&nbsp;&nbsp;
	<a href="#-Would-like-to-sync">Would like to sync?</a>&nbsp;&nbsp;&nbsp;
    <a href="#-Links">Links</a>
    </code>
</p>

<p align="center">
	<b> <sub>Check out my <a href="https://github.com/Sidd1609?tab=repositories"> <code>GitHub Repo</code> </a> or follow me on <a href="https://www.linkedin.com/in/sri-siddarth-chakaravarthy-p-145675192/"> <code>LinkedIn</code> </a> </sub></b>
</p>
<br>

<br>

## # Project Abstract

+ OpenCV is an open-source library developed mainly for real-time computer vision operations such as object detection, object tracking, etc. Currently, OpenCV supports trained models with benchmarked results on various datasets via its model_zoo. However, it only supports a limited number of models.

> <i> The aim of this project is to add object detection models such as Nanodet, EfficientDet, YOLOv5, etc. to the list of existing models in the OpenCV model zoo  to enable model inference using OpenCV python package</i>

<br>

## # Work Product

> A short video of the final product: 

<div align="center">Final Video Presentation
</div>


## # Pull Requests, Issues & Forks
**#** **Repository: opencv_zoo** [**`/working-branches`**](https://github.com/opencv/opencv_zoo/branches)
Forks
1. [opencv](https://github.com/Sidd1609/opencv_GSOC-22): [opencv] Forked the official OpenCV repository to try out examples and understand the <b>cv.dnn</b> framework offered by OpenCV on which the GSOC work revolves around. **`/ap`**

2. [EfficientDet](https://github.com/Sidd1609/EfficientDet-GSOC-): [signatrix] Forked the official EfficientDet model repo for working pre-trained model evaluation on the COCO val2017 dataset and learn the pre-process, inference and post-process modules of the model. **`/ap`**

3. [Nanodet](https://github.com/Sidd1609/Nanodet-GSOC): [RangiLyu] Forked the official Nanodet model repo for working pre-trained model evaluation on the COCO val2017 dataset and learn the pre-process, inference and post-process modules of the model. **`/ap`**

4. [YOLOX](https://github.com/Sidd1609/YOLOX-GSOC): [Megvii-BaseDetection] Forked the official YOLOX model repo for working pre-trained model evaluation on the COCO val2017 dataset and learn the pre-process, inference and post-process modules of the model. **`/ap`**

> <i> The final deliverable of this GSOC program was to help opencv_zoo support more light-weight object detection models so that developers will be able to infer models using <b>cv.dnn</b>  framework apart from existing model inference tools. This project also needed to satisfy the licensing of models used hence EfficientDet had not been pursued further. Finalized Models: NanoDet and YOLOX</i>

Pull requests created:

1. [opencv/opencv_zoo#75](https://github.com/opencv/opencv_zoo/pull/75): [opencv_zoo] Added NanodetPlus model to the OpenCV Zoo models stack **`/cp1`**

2. [opencv/opencv_zoo#86](https://github.com/opencv/opencv_zoo/pull/86): [opencv_zoo] Added YOLOX model to the OpenCV Zoo models stack **`/cp2`**

3. [opencv/opencv_zoo#91](https://github.com/opencv/opencv_zoo/pull/91): [opencv_zoo] Added COCO_Evaluation support in OpenCV Zoo tools **`/cp3`**

Issues opened:
1. [opencv/opencv_zoo#62](https://github.com/opencv/opencv_zoo/issues/62#-weekly-summary ): [opencv_zoo] This issue directs to this page which consists of the detailed information [about](url) this project and all the contributions made by myself during the course of GSOC'22 **`/cb`**

2. [Megvii-BaseDetection/YOLOX#1464](https://github.com/Megvii-BaseDetection/YOLOX/issues/1464): [YOLOX] This issue was raised to inform an issue related to add CPU evaluation support for YOLOX so that it can be easier to infer models and run benchmarks on CPU only devices**`/cp1`**

> **Tags**:
>
> **a**pplication **p**eriod : **`/ap`** <br>
> **c**ommunity **b**onding period : **`/cb`** <br>
> **c**oding **p**eriod **x** - **`/cpx`** <br>


- **Do the check issue tracker in the current repository for some more info.**

<br>

## # Weekly Summary
### Community Bonding - May 20th to June 12th, 2022

+ [Accepted for GSoC 2922 & 1st Meeting]
+ [A kick start meeting]

### Coding Period 1 - June 13th to  June 25th, 2022

+ Week#1: Object Detection with YOLOv5 and EfficientDet[Summary]

#### Done:
Created Task tracker issue on OpenCV_Zoo repo
Completed survey on object detection models and ran evaluation metrics on the COCO dataset. 
Model Evaluation on Google Colab and Local System (Nanodet and EfficientDet).
Converted Pytorch model to ONNX format.
Generated Nanodet model ONNX format with FP16.
Loaded the ONNX formatted model using OpenCV.

#### Plan:
Create Pull requests before mid-review for inferring the model using OpenCV.
Test the inferred model using OpenCV on sample images. 
Work on creating a quantized version of the ONNX model. 

#### Issues:
Not able to run inference using "Net. forward() on OpenCV despite being able to load and read the model layers using 
OpenCV. 

### Coding Period 2 - July 25th to  August 15th, 2022 
### Coding Period 3 - August 16th to  September 12th, 2022
<br>

## # Would like to sync?

+ We have planned to keep all the communication open 🎉 so that everyone can sync and is free to participate and help us grow! So if you have suggestions/comments about anything please do not hesitate to open up an [issue ticket]
+ 
+ There will be a weekly [blog post]

<br>

## # Links

+ GSoC project [proposal]
+ OpenCV: The Quest for Source Code Knowledge [paper](https://www.researchgate.net/publication/326942711_Graal_The_Quest_for_Source_Code_Knowledge)


<br>

### `Footnotes`

+ Work done during the application period can be found here : [Contributions]

