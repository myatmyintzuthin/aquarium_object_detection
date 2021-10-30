# Aquarium Object Detection :tropical_fish:
[![TensorFlow 2.6](https://img.shields.io/badge/TensorFlow-2.6-FF6F00?logo=tensorflow)](https://github.com/tensorflow/tensorflow/releases/tag/v2.6.0) 

Underwater Health Monitoring is an essential way to prevent extinction of sea animals and coral reef. In this repository, we will build an aquarium object detection system using Deep Learning and Computer Vision. 

![sample1.jpg](https://github.com/myatmyintzuthin/aquarium_object_detection/blob/main/assets/sample1.PNG)
![sample2.jpg](https://github.com/myatmyintzuthin/aquarium_object_detection/blob/main/assets/sample2.PNG)
------
#### Dataset
The [Aquarium Object Detection Dataset](https://public.roboflow.com/object-detection/aquarium) is collected by Brad Dwyer(Roboflow team) from two aquariums in the United States: The Henry Doorly Zoo in Omaha (October 16, 2020) and the National Aquarium in Baltimore (November 14, 2020). The dataset consists of 638 images splitted into train, test and validation data.

![train1.jpg](https://github.com/myatmyintzuthin/aquarium_object_detection/blob/main/assets/train1.jpg)
------
#### Model 
We will be using EfficientDet D0 model from [TensorFlow 2 Detection Model Zoo](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md). They provide a collection of detection models pre-trained on the [COCO 2017 dataset](https://cocodataset.org/).
| Model name  | Speed (ms)  | COCO mAP | Outputs |
| ----------- | ----------- | -------- | ------- |
| [EfficientDet D0 512x512](http://download.tensorflow.org/models/object_detection/tf2/20200711/efficientdet_d0_coco17_tpu-32.tar.gz)      | 39       | 33.6 | Boxes |
------
#### Metrics
After training for 4300 steps:
```
{'Loss/classification_loss': 0.18720163,
 'Loss/localization_loss': 0.08831813,
 'Loss/regularization_loss': 0.04052207,
 'Loss/total_loss': 0.31604183,
 'learning_rate': 0.07999277}
```
Validation Detection Metrics:

```
Accumulating evaluation results...
DONE (t=0.19s).
 Average Precision  (AP) @[ IoU=0.50:0.95 | area=   all | maxDets=100 ] = 0.324
 Average Precision  (AP) @[ IoU=0.50      | area=   all | maxDets=100 ] = 0.626
 Average Precision  (AP) @[ IoU=0.75      | area=   all | maxDets=100 ] = 0.298
 Average Precision  (AP) @[ IoU=0.50:0.95 | area= small | maxDets=100 ] = 0.022
 Average Precision  (AP) @[ IoU=0.50:0.95 | area=medium | maxDets=100 ] = 0.226
 Average Precision  (AP) @[ IoU=0.50:0.95 | area= large | maxDets=100 ] = 0.443
 Average Recall     (AR) @[ IoU=0.50:0.95 | area=   all | maxDets=  1 ] = 0.178
 Average Recall     (AR) @[ IoU=0.50:0.95 | area=   all | maxDets= 10 ] = 0.374
 Average Recall     (AR) @[ IoU=0.50:0.95 | area=   all | maxDets=100 ] = 0.449
 Average Recall     (AR) @[ IoU=0.50:0.95 | area= small | maxDets=100 ] = 0.063
 Average Recall     (AR) @[ IoU=0.50:0.95 | area=medium | maxDets=100 ] = 0.372
 Average Recall     (AR) @[ IoU=0.50:0.95 | area= large | maxDets=100 ] = 0.554
```
#### Tensor Board Metrics
![tensorboard.jpg](https://github.com/myatmyintzuthin/aquarium_object_detection/blob/main/assets/tensorboard.PNG)
------
#### References
[Custom object detection in the browser using TensorFlow.js by Hugo Zanini](https://blog.tensorflow.org/2021/01/custom-object-detection-in-browser.html) \
[TensorFlow Object Detection API Tutorial](https://readthedocs.org/projects/tensorflow-object-detection-api-tutorial/) \
[TensorFlow 2 Detection Model Zoo](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md)

 





