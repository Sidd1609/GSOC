## # Week-1 Summary

#### Preview
- I had previous experience working with object detection models. Hence, I was familiar with training models and evaluating trained models using pytorch and tensorflow frameworks using python. However, for this contribution I had to learn adpat to using <b>cv.dnn</b> framework since the entire project revolved providing more opencv zoo features based on opencv frameworks.
- Therefore, I was asked to review work with <b>cv.dnn</b> framework by trying out examples from the opencv_zoo repo and also refering to the package and module informations from [opencv](https://docs.opencv.org/3.4/d6/d0f/group__dnn.html) documentation
- This project involved working on trained model weights, hence I was not required to open a lot of pull request making my contributions very precise to the point. I was assigned the following tasks for the week ahead.

<b>WEEK1 TASKS</b>
- [x] Create Task tracker issue on OpenCV_Zoo repo
- [x] Complet survey on light-weight object detection models and run evaluation on COCO dataset. 


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
