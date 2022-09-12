## # Week-3 Summary

#### PREVIEW
###### Total Hours Spent: 18 hours 🟩🟩🟩🟩🟩🟩
###### Commits: None
###### Pull Requests: None 
###### Project Status: ![25%](https://progress-bar.dev/25)


- I had started working on Nanodet Inference using openCV's Deep Neural Network framework <b>(cv.dnn)</b>. I began testing various models from the Nanodet repo including the legacy models. 
- For the project, we made use of the <b>NanoDet-Plus-m-1.5x</b> version of Nanodet model since it offers the following advantages over other models.

| Resolution | mAPval (0.5:0.95) | CPU Latency (i7-8700) | ARM Latency (4xA76) | FLOPS | Params | Model Size |
|:-----------|:------------------|:----------------------|:--------------------|:------|--------|:-----------|
| 416*416 | 34.1 | 11.50ms |	25.49ms | 2.97G |	2.44M	| 4.7MB(FP16) & 2.3MB(INT8) |
	
- In NanoDet-Plus, we propose a novel label assignment strategy with a simple assign guidance module (AGM) and a dynamic soft label assigner (DSLA) to solve the optimal label assignment problem in lightweight model training. We also introduce a light feature pyramid called Ghost-PAN to enhance multi-layer feature fusion. These improvements boost previous NanoDet's detection accuracy by 7 mAP on COCO dataset. 


<b>WEEK3 TASKS</b>
- [x] Demonstrated <b>cv.dnn</b> inference of nanodet on test images from val2017 COCO dataset.[work](https://colab.research.google.com/drive/1VpRHzBwP2wanYv6nkKOTOZN_5V7ev-c2?usp=sharing)
- [x] Run benchmark of the model on COCO val2017 dataset and report the scores for Average Precision (AP) and Average Recall (AR), the results observed are shared below. 

<table>
<tr><th>Average Precision </th><th>Average Recall</th></tr>
<tr><td>
  
|  area  |  IoU  |  Average Precision(AP)  |
|:-------|:------|:------------------------|
|  all  |  0.50:0.95  |  0.304  |
|  all  |  0.50  |  0.459  |
|  all  |  0.75  |  0.317  |
|  small  |  0.50:0.95  |  0.107  |
|  medium  |  0.50:0.95  |  0.322  |
|  large  |  0.50:0.95  |  0.478  |
 
 </td><td>

  area  |  IoU  |  Average Recall  |
|:-------|:------|:----------------|
|  all  |  0.50:0.95  |  0.278  |
|  all  |  0.50:0.95  |  0.434  |
|  all  |  0.50:0.95 |  0.462  |
|  small  |  0.50:0.95  |  0.198  |
|  medium  |  0.50:0.95  |  0.510  |
|  large  |  0.50:0.95  |  0.702  |
</td></tr> </table>

- [x] Evaluate model precision metrics on val2017 dataset and report scores for individual class labels. Below are the precision scores observed per class. 

| class         | AP50   | mAP   | class          | AP50   | mAP   |
|:--------------|:-------|:------|:---------------|:-------|:------|
| person        | 67.5   | 41.8  | bicycle        | 35.4   | 18.8  |
| car           | 45.0   | 25.4  | motorcycle     | 58.9   | 33.1  |
| airplane      | 77.3   | 58.9  | bus            | 68.8   | 56.4  |
| train         | 81.1   | 60.5  | truck          | 38.6   | 24.7  |
| boat          | 35.5   | 16.7  | traffic light  | 30.5   | 14.0  |
| fire hydrant  | 69.8   | 54.5  | stop sign      | 60.9   | 54.6  |
| parking meter | 55.1   | 38.5  | bench          | 26.8   | 15.9  |
| bird          | 38.3   | 23.6  | cat            | 82.5   | 62.1  |
| dog           | 67.0   | 51.4  | horse          | 64.3   | 44.2  |
| sheep         | 57.7   | 35.8  | cow            | 61.2   | 39.9  |
| elephant      | 79.9   | 56.2  | bear           | 81.8   | 63.0  |
| zebra         | 85.4   | 59.5  | giraffe        | 84.1   | 59.9  |
| backpack      | 12.4   | 5.9   | umbrella       | 46.5   | 28.8  |
| handbag       | 8.4    | 3.7   | tie            | 35.2   | 19.6  |
| suitcase      | 38.1   | 23.8  | frisbee        | 60.7   | 43.9  |
| skis          | 30.5   | 14.5  | snowboard      | 32.3   | 18.2  |
| sports ball   | 37.6   | 24.5  | kite           | 51.1   | 30.4  |
| baseball bat  | 28.9   | 13.6  | baseball glove | 40.1   | 21.6  |
| skateboard    | 59.4   | 35.2  | surfboard      | 47.9   | 26.6  |
| tennis racket | 55.2   | 30.5  | bottle         | 34.7   | 20.2  |
| wine glass    | 27.8   | 16.3  | cup            | 35.5   | 23.7  |
| fork          | 25.9   | 14.8  | knife          | 10.9   | 5.6   |
| spoon         | 8.7    | 4.1   | bowl           | 42.8   | 29.4  |
| banana        | 35.5   | 18.5  | apple          | 19.4   | 12.9  |
| sandwich      | 46.7   | 33.4  | orange         | 35.2   | 25.9  |
| broccoli      | 36.4   | 19.1  | carrot         | 30.9   | 17.8  |
| hot dog       | 42.7   | 29.3  | pizza          | 61.0   | 44.9  |
| donut         | 47.3   | 34.0  | cake           | 39.9   | 24.4  |
| chair         | 28.8   | 16.1  | couch          | 60.5   | 42.6  |
| potted plant  | 29.0   | 15.3  | bed            | 63.3   | 46.0  |
| dining table  | 39.6   | 27.5  | toilet         | 71.3   | 55.3  |
| tv            | 66.5   | 48.1  | laptop         | 62.6   | 46.9  |
| mouse         | 63.5   | 44.1  | remote         | 19.8   | 10.3  |
| keyboard      | 62.1   | 41.5  | cell phone     | 33.7   | 22.8  |
| microwave     | 54.9   | 39.6  | oven           | 48.1   | 30.4  |
| toaster       | 30.0   | 16.4  | sink           | 44.5   | 27.8  |
| refrigerator  | 63.2   | 46.1  | book           | 18.4   | 7.3   |
| clock         | 57.8   | 35.8  | vase           | 33.7   | 22.1  |
| scissors      | 27.8   | 17.8  | teddy bear     | 54.1   | 35.4  |
| hair drier    | 2.9    | 1.1   | toothbrush     | 13.1   | 8.2   |


##### Note
🟩 - 3 hours of coding (working days: Monday - Saturday)

