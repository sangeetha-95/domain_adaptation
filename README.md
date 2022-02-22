# Domain adaptation in deep learning object detection models

Object detection models in deep learning have achieved major milestones in the recent years. The strength of these models are in their ability to analyze data containing objects and identifying what constitutes those objects. These models are trained and tested on large quantity of data for achieving their optimal performance. The identification of objects is affected by the quality of the collected data and it will be biased if the data contains few objects more frequently. Domain adaptation has been introduced to help with these challenges on the availability and quality of data. It consists of techniques to either adapt the model to train on the substandard data available or create necessary quantity of ideal data to train. These techniques can be categorized into two major groups. The first technique is manipulating the model to train on the available data, which is a single step procedure as it creates an end to end training framework. The second technique creates a new training data from an existing non ideal training data, which is a multi step approach. 

This project focuses primarily on analyzing the performance of these two domain adaptation techniques on object detection models. Initially, a theoretical analysis of existing domain adaptation techniques is conducted to understand their preliminaries. Later, a single step unsupervised domain adaptation model and a multi step weakly supervised domain adaptation model are trained and tested on natural as well as artistic domain datasets. Finally, an experimental evaluation is conducted on the basis of inference results, individual object class AP scores and final mAP score of trained detector models to analyze the detection performance and understand its drawbacks. The final results will show that the multi step weakly supervised method addressing the domain shift through multiple training steps has higher inference results than the end to end training model.   

## Single Step Unsupervised Domain Adaptation

### Synthetic to Natural Domain Adaptation

| Domains | mAP | mAP_50 | Trained model |
| ------ | ------ | ------ | ------ |
| SIM10K | 40.1 | 67.2 | [model](https://tubcloud.tu-berlin.de/apps/files/?dir=/Sangeetha_Reji_Master_Thesis/mmdetection&fileid=3178405934)
| Cityscapes | 15.8 | 32.9 | 

### Natural to Natural Domain Adaptation

| Domains | mAP | mAP_50 | Trained model |
| ------ | ------ | ------ | ------ |
| Cityscapes | 7.99 | 16.43 |  [model](https://tubcloud.tu-berlin.de/s/EXwR5AngoFQzHrR)
| Foggy Cityscapes| 6.25 | 13.30 | 



## Multi Step Weakly Supervised Domain Adaptation

| Detector and number of iterations | Clipart1K | Watercolor2k | Comic2k | Trained model |
| ------ | ------ | ------ | ------ | ------ |
| Pretrained | 45.97 | 54.25 | 37.24 |  [model](https://tubcloud.tu-berlin.de/s/C4morDjosz6922Y)
| SSD300 5000 iterations | 42.36 | 52.57 | 37.62 |  [model](https://tubcloud.tu-berlin.de/s/C4morDjosz6922Y)
| SSD300 10000 iterations | 43.48 | 53.28 | 37.50 |  [model](https://tubcloud.tu-berlin.de/s/C4morDjosz6922Y)
| SSD300 15000 iterations| 43.24 | 52.11 | 36.38 |  [model](https://tubcloud.tu-berlin.de/s/C4morDjosz6922Y)
| SSD512 5000 iterations | 44.11 | 52.56 | 35.61|  [model](https://tubcloud.tu-berlin.de/s/C4morDjosz6922Y)
| SSD512 10000 iterations | 43.21 | 51.50 | 35.78 |  [model](https://tubcloud.tu-berlin.de/s/C4morDjosz6922Y)
| SSD512 15000 iterations| 43.46 | 50.98 | 35.26 |  [model](https://tubcloud.tu-berlin.de/s/C4morDjosz6922Y)


## Multi Step Weakly Supervised Domain Adaptation using MMDetection


| Detector | Clipart1K | Watercolor2k | Comic2k |Trained model |
| ------ | ------ | ------ | ------ | ------ |
| FCOS R101 | 22.9 | 50.5 | 36.6 |  [model](https://tubcloud.tu-berlin.de/s/bazfmE8DTMNa3Sw)
| Faster R-CNN R101 | 20.6 | 34.0 | 14.7 |  [model](https://tubcloud.tu-berlin.de/s/bazfmE8DTMNa3Sw)
| Faster R-CNN X101 | 58.8 | 61.1 | 46.6 |  [model](https://tubcloud.tu-berlin.de/s/bazfmE8DTMNa3Sw)
| Cascade R-CNN X101| 50.0 | 57.9 | 46.2 |  [model](https://tubcloud.tu-berlin.de/s/bazfmE8DTMNa3Sw)
