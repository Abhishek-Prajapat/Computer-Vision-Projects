# Casava Leaf Disease Classification
It is a image classification challenge where given a image you have to identify which class the given image belongs to. <br> <br>

The dataset can be downloaded from here - <a href="https://www.kaggle.com/c/cassava-leaf-disease-classification/data">here</a>

My main purpose in doing this project is to apply various state-of-art models on this problem and study their results.
For this task I have use the follwing models and configuration:-

Model | Input image size | Test set ROC
------|------------------|----
ResNext | 256*256 | 0.958
EfficientNet | 256*256 | 0.9523
Vision Transformer | 224*224 | 0.9444

The basic Exploratory Data Analysis can also be found in the codes.

As my objective was to study these models and their implimentations and also due to lack of Computational resources I have limited the project to only a train and test set and hence no validation set has been used. All the finetuning has been done on the test set only.