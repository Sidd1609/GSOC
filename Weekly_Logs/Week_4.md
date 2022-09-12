## # Week-4 Summary

#### Preview
###### Total Hours Spent this week: 15 hours 🟩🟩🟩🟩🟩
###### Commits: None
###### Pull Requests: None
###### Project Status: ![40%](https://progress-bar.dev/40)


- After completing model inference using opencv's <b>cv2.dnn</b> framework, I needed to export the evaluated model into .ONNX format. This included converting the model from an FP32 to FP16 format. 
- Needed to evaluate the FP16 formatted .ONNX model using <b>cv2.dnn</b> framework and check if it can be infered using opencv 
  
  - NanoDet.pth/Nanodet.ckpt: The original repo only offered a pytorch model with its config file. The config file had parameters needed for converting the model to FP16 using <b>torch.export</b> module.
  
  - NanoDet.onnx: This is the .ONNX formatted model in FP16 which is used for adding the model to the opencv_zoo library, this model is later used for quantization to offer developers with more quantised version of NanoDet in int8. 


<b>WEEK4 TASKS</b>
- [x] Covert pytorch model to onnx using torch.export
- [x] Evaluate onnx model on inference dataset (COCO val2017)
- [x] Infer the onnx model using cv2.dnn

