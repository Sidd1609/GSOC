## # Week-11 Summary

#### PREVIEW
###### Total Hours Spent: 21 hours 🟩🟩🟩🟩🟩🟩🟩
###### Commits: 2
###### Pull Requests: 2
###### Project Status: ![100%](https://progress-bar.dev/100)


- This was the final drive in the GSoC 2022 program. I was only left with the Quantization of models using the onnxruntime <b>static_quantize()</b> tool. Previously I had worked with dynamic quantization using Intel's OpenVino ToolKit which gave me a general idea on model quantization. I had first refered the onnxruntime repository and worked around with some examples provided and learned the use of the parameters. 
- A quantized model executes some or all of the operations on tensors with reduced precision rather than full precision (floating point) values. This allows for a more compact model representation and the use of high performance vectorized operations on many hardware platforms.
- In this project, I worked on quantising a FP16 model to an int8 model. Here we worked on quantisation for both NanoDet and YoloX. 
- Quantisation of models help in reducing computation demand and increasing power efficiency. The fundamental idea behind quantization is that if we convert the weights and inputs into integer types, we consume less memory and on certain hardware, the calculations are faster.
- Quantisation levels are pre-determined levels, like the rungs of a ladder, between the lowest possible sample value and the highest. The closeness of the approximation between a sample value and its nearest quantisation level depends on the number of quantisation levels available.

<b>WEEK11 TASKS</b>
- [x] Work with onnxruntime tool and review examples in the official repository. 
- [x] Quantise NanoDet model from FP16 to int8 using static_quantise().
- [x] Quantise YoloX model from FP16 to int8 using static_quantise().
- [x] Run evaluation and inference on quantised models.
- [x] Upload the quantised models to respective branches and PRs.


<b>BRANCH</b>
- [x] [gsoc_nanodet](https://github.com/Sidd1609/opencv_zoo/tree/gsoc_nanodet)
- [x] [gsoc_yolox](https://github.com/Sidd1609/opencv_zoo/tree/gsoc_yolox)


<b>PULL REQUEST</b>
- [x] [PR#87](https://github.com/opencv/opencv_zoo/pull/87)
- [x] [PR#86](https://github.com/opencv/opencv_zoo/pull/86)


<b>COMMITS</b>
- [x] [nanodet_quant_int8](https://github.com/opencv/opencv_zoo/commit/bddffc7b797567d56f2d6a37fa896c2ebb652c73)
- [x] [yolox_s_quant_int8](https://github.com/opencv/opencv_zoo/commit/99eb50a572e8798c20d918ff1a3216705eb7b99b)


<b>ISSUE</b>
- [x] [issue](https://github.com/opencv/opencv_zoo/issues/62)


##### Note
🟩 - 3 hours of coding (working days: Monday - Sunday)
