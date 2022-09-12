## # Week-3 Summary

#### Preview
- I had started working on Nanodet Inference using openCV's Deep Neural Network framework <b>(cv.dnn)</b>. I began testing various models from the Nanodet repo including the legacy models. 
- For the project, we made use of the <b>NanoDet-Plus-m-1.5x</b> version of Nanodet model since it offers the following advantages over other models.

| Resolution | mAPval (0.5:0.95) | CPU Latency (i7-8700) | ARM Latency (4xA76) | FLOPS	Params | Model Size |
|:-----------|:------------------|:----------------------|:--------------------|:--------------|:-----------|
| 416*416 | 34.1 | 11.50ms |	25.49ms | 2.97G |	2.44M	| 4.7MB(FP16) & 2.3MB(INT8) |
	
- In NanoDet-Plus, we propose a novel label assignment strategy with a simple assign guidance module (AGM) and a dynamic soft label assigner (DSLA) to solve the optimal label assignment problem in lightweight model training. We also introduce a light feature pyramid called Ghost-PAN to enhance multi-layer feature fusion. These improvements boost previous NanoDet's detection accuracy by 7 mAP on COCO dataset. 

<b>WEEK3 TASKS</b>
- [x] Demonstrate <b>cv.dnn</b> inference of nanodet on test images from val2017 COCO dataset.
- [x] Evaluate model precision metrics on val2017 dataset and report scores. 
