## # Week-5 Summary

#### Preview
###### Total Hours Spent: 15 hours 🟩🟩🟩🟩🟩
###### Commits: 80
###### Pull Requests: 1 
###### Project Status: ![50%](https://progress-bar.dev/50)


- After completing model inference using opencv's <b>cv2.dnn</b> framework, I had to create a pull request and add NanoDet model to openCV's model_zoo library. 
- I had to work on the following modules to infer an NanoDet model in opencv zoo library. The following modules were shceduled to be completed in the coming weeks and complete the [object_detection_nanodet](https://github.com/Sidd1609/opencv_zoo/tree/gsoc_nanodet/models/object_detection_nanodet) in the gsoc_nanodet branch. This branch only includes work pertaining to NanoDet model.
  - NanoDet.py
    - Pre_process: This module in Nanodet.py should be able to pre-process a given image by scaling the image to the parameters of Nanodet-m-plus-1.5x_416, this included resizing images to a resolution of 416 x 416 then creating input blobs of the image data using <b>cv2.dnn.blobFromImage()</b> module from <b>cv.dnn</b> framework. This module then returns the blob data of the inference image to the infer module.
  
    - Infer: This module then sets the input blob as input for the onnx formatted model that was loaded using <b>cv2.dnn.readNetFromONNX() or cv2.dnn.readNet()</b> with <b>net.setInput()</b>. After setting the input, we need to execute the model's layers which is done using <b>net.forward(net.getUnconnectedOutLayersNames())</b> where net is the variable that contains the loaded model. This module from <b>cv2.dnn</b> framework will return predictions in the form of a single multi-dimensional numpy array that includes scores, bounding-box coordinates, and class labels. This out needs to be processed so that we can get formatted outputs of individual components such as scores, bounding-box coordinates, and class labels. This is done by the post_process module.
   
    - Post_process: This module inputs the output from <b>net.forward(net.getUnconnectedOutLayersNames())</b> and processes the output to return scores, bounding-box coordinates, and class labels of predicitons that have confidence value more than the threshold set for detection (by default prob_threshold=0.35, iou_threshold=0.6). This module parses the output multi-dimensional array to filter out predictions with confidence values higher than the threshold and returns unscaled values for bounding-box coordinates along with the scores and class labels of the detections in the image.
    
  - Demo.py
    - Input: The demo.py supports two type of input format for model inference namely an input image or a user's webcam for video inference. We establish an argument parser to get inputs for test inference which include parameters such as input type, input data, confidence threshold, IOU threshold and the option to save the inference result. Then we process the input image or frame from webcam by converting the captured data to RGB scale using <b>cv2.cvtColor(image, cv2.COLOR_BGR2RGB)</b> since the model requires input to be in this particular format. Then we run the model inference by calling the infer module which pre-processes the image and returns the post-processed outputs. 
   
    - Output_Visualization: This module in demo.py is used to scale the bounding box coordinates back to the images resolution, and then visualize the predicitons by plotting boxes using <b>cv2.rectangle()</b>. This module is required so that the bounding boxes are formatted properly for each individual image allowing the model to inference images with different resolutions. 

<b>WEEK5 TASKS</b>
- [x] Create pull request in opencv_zoo repo for [object_detection_nanodet](https://github.com/opencv/opencv_zoo/pull/87)
- [x] Complete NanoDet.py modules
  - [x] Pre_process
  - [x] Infer
  - [x] Post_process
- [x] Test sample images for inference using the NanoDet.py script. 


<b>COMMITS</b>
- [Nanodet.py](https://github.com/opencv/opencv_zoo/pull/87/commits/82c5161bf6bc1bdc57e9021e6a7b65108bf39ef4)
- [ReadME](https://github.com/opencv/opencv_zoo/pull/87/commits/ede0f6965c6d41c90b1f0887af573f5f5185b97f)
