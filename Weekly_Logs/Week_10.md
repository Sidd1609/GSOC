## # Week-10 Summary

#### PREVIEW
###### Total Hours Spent: 21 hours 🟩🟩🟩🟩🟩🟩🟩
###### Commits: 126
###### Pull Requests: 1 
###### Project Status: ![90%](https://progress-bar.dev/90)


- Since I had already worked on Nanodet inference and created a pull request for Nanodet model, It was easy to adapt the same coding templates for the modules for YoloX. After completing model inference using opencv's <b>cv2.dnn</b> framework, I created a pull request and add YoloX model to openCV's model_zoo library. 
- I had to work on the following modules to infer an YoloX model in opencv zoo library. The following modules were shceduled to be completed in the coming weeks and complete the [object_detection_yolox](https://github.com/Sidd1609/opencv_zoo/tree/gsoc_yolox) in the gsoc_yolox branch. This branch only includes work pertaining to YoloX model.
  - YoloX.py
    - Pre_process: This module in YoloX.py should be able to pre-process a given image by scaling the image to the parameters of YoloX_s, YoloX_tiny or YoloX_nano this included resizing images to a resolution of 640 x 640 or 416 x 416 then creating input blobs of the image data using <b>cv2.dnn.blobFromImage()</b> module from <b>cv.dnn</b> framework. This module then returns the blob data of the inference image to the infer module.
  
    - Infer: This module then sets the input blob as input for the onnx formatted model that was loaded using <b>cv2.dnn.readNetFromONNX() or cv2.dnn.readNet()</b> with <b>net.setInput()</b>. After setting the input, we need to execute the model's layers which is done using <b>net.forward(net.getUnconnectedOutLayersNames())</b> where net is the variable that contains the loaded model. This module from <b>cv2.dnn</b> framework will return predictions in the form of a single multi-dimensional numpy array that includes scores, bounding-box coordinates, and class labels. This out needs to be processed so that we can get formatted outputs of individual components such as scores, bounding-box coordinates, and class labels. This is done by the post_process module.
   
    - Post_process: This module inputs the output from <b>net.forward(net.getUnconnectedOutLayersNames())</b> and processes the output to return scores, bounding-box coordinates, and class labels of predicitons that have confidence value more than the threshold set for detection (by default confThreshold=0.35, nmsThreshold=0.5, objThreshold=0.5). This module parses the output multi-dimensional array to filter out predictions with confidence values higher than the threshold and returns unscaled values for bounding-box coordinates along with the scores and class labels of the detections in the image.
    
  - Demo.py
    - Input: The demo.py supports two type of input format for model inference namely an input image or a user's webcam for video inference. We establish an argument parser to get inputs for test inference which include parameters such as input type, input data, confidence threshold, IOU threshold and the option to save the inference result. Then we process the input image or frame from webcam by converting the captured data to RGB scale using <b>cv2.cvtColor(image, cv2.COLOR_BGR2RGB)</b> since the model requires input to be in this particular format. Then we run the model inference by calling the infer module which pre-processes the image and returns the post-processed outputs. 
   
    - Output_Visualization: This module in demo.py is used to scale the bounding box coordinates back to the images resolution, and then visualize the predicitons by plotting boxes using <b>cv2.rectangle()</b>. This module is required so that the bounding boxes are formatted properly for each individual image allowing the model to inference images with different resolutions. 
- Now I had to work on the Demo.py file which needed to load the trained .ONNX model and use the modules: pre_process, infer, post_process from the NanoDet.py to run inference on test images. 
- I also had to provide webcam support for users in the demo.py file which was done using <b>cv2.capture()</b> The following modules were completed to be completed in this week before the mid-term evaluation [object_detection_yolox](https://github.com/Sidd1609/opencv_zoo/tree/gsoc_yolox) in the gsoc_yolox branch. This branch only includes work pertaining to YoloX model.
- I also had to work on allowing users to save the results they test on the models to their local dir in which they had cloned the repo. I used the <b>cv2.VideoWriter()</b> for performing this functionality and integrated to Nanodet's repo in model zoo. 

<b>WEEK10 TASKS</b>
- [x] Create pull request in opencv_zoo repo for [object_detection_yolox](https://github.com/opencv/opencv_zoo/pull/86)
- [x] Complete YoloX.py modules
  - [x] Pre_process
  - [x] Infer
  - [x] Post_process
- [x] Test sample images for inference using the YoloX.py script. 
- [x] Complete YoloX pull request and complete model inference using opencv.
- [x] Add webcam support. 
- [x] Add feature for save that will allow users to save results. 
- [x] Remove class labels file in directory and add it directly into demo.py for faster inference.


<b>BRANCH</b>
- [x] [gsoc_yolox](https://github.com/Sidd1609/opencv_zoo/tree/gsoc_yolox)


<b>PULL REQUEST</b>
- [x] [PR#86](https://github.com/opencv/opencv_zoo/pull/86)


<b>COMMITS</b>
- [x] [demo_py](https://github.com/opencv/opencv_zoo/pull/86/files/d45793af470d0b5a120fcaf9e4060b5f33bdb8e0#diff-25489df2835b5d21ed14a81aee33cdca259098d37fb0441ab76e1d9134eaf1a0)
- [x] [YoloX_py](https://github.com/opencv/opencv_zoo/pull/86/files/d45793af470d0b5a120fcaf9e4060b5f33bdb8e0#diff-e00ac7b5ef6f02331aac9d5b854ce37b7f6c8cbaa60aeb376a8c5bec75b26f07)
- [x] [ReadMe](https://github.com/opencv/opencv_zoo/pull/86/files/d45793af470d0b5a120fcaf9e4060b5f33bdb8e0#diff-c0d7c0d31ca9c725e7bf5f7236e518fa03127b114339413d65766c4f4d50585d)
- [x] [License](https://github.com/opencv/opencv_zoo/pull/86/files/d45793af470d0b5a120fcaf9e4060b5f33bdb8e0#diff-01e21a0c3943c56141120d9f85c1da959e280bff84e3992de2b67a88f7d0c41e)
- [x] [Test_Inference](https://github.com/opencv/opencv_zoo/pull/86/files/d45793af470d0b5a120fcaf9e4060b5f33bdb8e0#diff-e0b5e4201a96df902a7b92d7e62f60fd79de20b546cef7c556c331b6961658cf)


##### Note
🟩 - 3 hours of coding (working days: Monday - Sunday)
