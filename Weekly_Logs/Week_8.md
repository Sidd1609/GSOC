## # Week-8 Summary

#### PREVIEW
###### Total Hours Spent: 15 hours 🟩🟩🟩🟩🟩
###### Commits: None
###### Pull Requests: None
###### Project Status: ![65%](https://progress-bar.dev/65)


- In continuation to previous week, this week I worked on creating an analysis sheet for jotting down individual precision metrics for trained model weights. Most model repos had various versions of the model. Hence, I worked on evaluation of all variations to accumulate overall results that would help to finalize models that needed to be added to the model zoo library. 
- I worked on testing versions of YoloX such as: YoloX_s, YoloX_tiny, YoloX_nano.


<b>WEEK8 TASKS</b> 
- [x] Model(s) evaluation using COCO val2017 dataset in Google Colab(With CPU and GPU). 
- [x] Model inference on test image from COCO val2017 dataset in Google Colab.


<b>CHALLENGES</b>
- Model inference and evaluation of YoloX using only CPU was not offered by the official repo. The wrapper classes and the pre-processing functions where written in tensorflow that incorporated GPU tensors for accumulating prediction results. 
- Hence, I needed to opt for Google Colab, another alternative was to use M1 chip for accelerating GPU applications in the program, but some of the accelerating support for Apple's M series chips are still in development. Therefore, I proceeded with google colab.


<b>ISSUE</b>
- [x] [Megvii-BaseDetection/YOLOX#1464](https://github.com/Megvii-BaseDetection/YOLOX/issues/1464): [YOLOX] This issue was raised to inform an issue related to adding CPU evaluation support for YOLOX so that it can be easier to infer models and run benchmarks on CPU only devices.


<b>Work</b>
- [x] [Colab](https://colab.research.google.com/drive/1qABb90X0mNBnEd8u1JBTvRiizvmZxIT2?usp=sharing)


##### Note
🟩 - 3 hours of coding (working days: Monday - Friday)
