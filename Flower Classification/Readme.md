# Flower Classification
This dataset is given in a tfrecord format. This was my first introduction to this format and I learned how to use it. In this problem I had to classify give a flower which class does it belong to from 104 classes.

The dataset for the problem can be found <a href="https://www.kaggle.com/c/tpu-getting-started/data">here</a>.

I trained 2 models using **TensorFlow** for this task and use a train set for training and validation set for validating and finetuning and a test set for predicting the output which gave me following results (As the models are saved with least validation loss I will write the corresponding training loss):

Model | Training (Loss) | Validation (Loss) | Test (F1 Score)
------|----------|------------|------
Vision Transformer | 0.1198 | 0.2793 | 0.94706
ResNet | 0.1003 | 0.3631 | 0.90035

Both the models are overfitting on the training data and could use even more regularization but as model training is a iterative process I will stop here for now.

In case you want to check the logs and get the trained model you can find them <a href="https://drive.google.com/drive/folders/1LgtzfwyLX0mUNVFeh4F1tmKTbI0ya6M_?usp=sharing">here</a>.

The Notebooks are following:
* Exploratory Data Analysis
* Training Vision Transformer
* Training ResNet
* Inference:
  * Contains the plots of learning curves of both the models
  * Contains the prediction on test set

**Note**: The submission folder contains the predicited files on test set.