# SIIM-FISABIO-RSNA COVID-19 Detection

In this problem you are provided with a study over a patient and you have to identify if that study is abnormal or not. In each study there are several dicom files of the patient and each file contains a pixel array which contains the image of the chest and lungs which radiologists use to identify.
Also Given each image you have to do object-detection and create a bounding box over the area of abnoramlity if the abnormality exists. Below are 2 sample images from the dataset.

<img src="./Sample.PNG">

The problem was very challanging as there were really few positive samples which is usually the case with medical images. To hande it I used various techniques such as **`Pre-Training`** the classifier on a similar dataset. **`Augmentation`** and last but not least **`OverSampling`** for object detection and **`Loss-Weight-Adjustment`** for classifier of positive images.

For the following problem I created the gigantic model of **`EfficientNetB7`** and trained over a `tpu` on kaggle.
The results are over a 2fold validation.
AUC | loss
----|------
0.805 | 0.3752

For the purpose of object-detection I trained a **`YOLOv5`** Model which provided the following results.
Precision | Recall | mAP@0.5 | Total Loss | Epochs
-------|-------|-------|-------|-------|
0.575 | 0.453 | 0.444 | 0.0706 | 9

The resuls of the `Yolov5` can also be seen <a href="https://wandb.ai/abhishek_prajapat/kaggle-siim-covid?workspace=">here</a>. These contains results of my multiple runs.

I also studies other models and their performance on the same problem but these models were performing the best respectively.