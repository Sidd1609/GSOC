## # Week-6 Summary

#### PREVIEW
###### Total Hours Spent: 18 hours 🟩🟩🟩🟩🟩🟩
###### Commits: 127
###### Pull Requests: 1 
###### Project Status: ![50%](https://progress-bar.dev/50)


- Now I had to work on the Demo.py file which needed to load the trained .ONNX model and use the modules: pre_process, infer, post_process from the NanoDet.py to run inference on test images. 
- I also had to provide webcam support for users in the demo.py file which was done using <b>cv2.capture()</b> The following modules were completed to be completed in this week before the mid-term evaluation [object_detection_nanodet](https://github.com/Sidd1609/opencv_zoo/tree/gsoc_nanodet/models/object_detection_nanodet) in the gsoc_nanodet branch. This branch only includes work pertaining to NanoDet model.

  - NanoDet.py
    - Pre_process: This module in Nanodet.py should be able to pre-process a given image by scaling the image to the parameters of Nanodet-m-plus-1.5x_416, this included resizing images to a resolution of 416 x 416 then creating input blobs of the image data using <b>cv2.dnn.blobFromImage()</b> module from <b>cv.dnn</b> framework. This module then returns the blob data of the inference image to the infer module.
  
    - Infer: This module then sets the input blob as input for the onnx formatted model that was loaded using <b>cv2.dnn.readNetFromONNX() or cv2.dnn.readNet()</b> with <b>net.setInput()</b>. After setting the input, we need to execute the model's layers which is done using <b>net.forward(net.getUnconnectedOutLayersNames())</b> where net is the variable that contains the loaded model. This module from <b>cv2.dnn</b> framework will return predictions in the form of a single multi-dimensional numpy array that includes scores, bounding-box coordinates, and class labels. This out needs to be processed so that we can get formatted outputs of individual components such as scores, bounding-box coordinates, and class labels. This is done by the post_process module.
   
    - Post_process: This module inputs the output from <b>net.forward(net.getUnconnectedOutLayersNames())</b> and processes the output to return scores, bounding-box coordinates, and class labels of predicitons that have confidence value more than the threshold set for detection (by default prob_threshold=0.35, iou_threshold=0.6). This module parses the output multi-dimensional array to filter out predictions with confidence values higher than the threshold and returns unscaled values for bounding-box coordinates along with the scores and class labels of the detections in the image.
    
  - Demo.py
    - Input: The demo.py supports two type of input format for model inference namely an input image or a user's webcam for video inference. We establish an argument parser to get inputs for test inference which include parameters such as input type, input data, confidence threshold, IOU threshold and the option to save the inference result. Then we process the input image or frame from webcam by converting the captured data to RGB scale using <b>cv2.cvtColor(image, cv2.COLOR_BGR2RGB)</b> since the model requires input to be in this particular format. Then we run the model inference by calling the infer module which pre-processes the image and returns the post-processed outputs. 
   
    - Output_Visualization: This module in demo.py is used to scale the bounding box coordinates back to the images resolution, and then visualize the predicitons by plotting boxes using <b>cv2.rectangle()</b>. This module is required so that the bounding boxes are formatted properly for each individual image allowing the model to inference images with different resolutions. 

- I also had to work on allowing users to save the results they test on the models to their local dir in which they had cloned the repo. I used the <b>cv2.VideoWriter()</b> for performing this functionality and integrated to Nanodet's repo in model zoo. 


<b>WEEK6 TASKS</b>
- [x] Complete NanoDet pull request and complete model inference using opencv.
- [x] Add webcam support. 
- [x] Add feature for save that will allow users to save results. 
- [x] Remove class labels file in directory and add it directly into demo.py for faster inference.
- [x] Complete GSoC contributor [Mid-term evaluations.](https://summerofcode.withgoogle.com/evaluations/1LJv9isH) 


<b>BRANCH</b>
- [x] [gsoc_nanodet](https://github.com/Sidd1609/opencv_zoo/tree/gsoc_nanodet)


<b>PULL REQUEST</b>
- [x] [PR#87](https://github.com/opencv/opencv_zoo/pull/87)


<b>COMMITS</b>
- [x] [demo_py](https://github.com/opencv/opencv_zoo/pull/87/commits/078c4eb5bd262eebc92dc07c8a5833a62bc76669)


##### Note
🟩 - 3 hours of coding (working days: Monday - Saturday)
