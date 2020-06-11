# CNN-Image-Classification-Pneumonia
Pneumonia Image Classification from https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia
(unfortunately the dataset and model weigh more than 1 gigabyte and therefore are not represented in this repository)

You need to download the dataset from kaggle, and then extract the files (unzip).

unzip /path/to/17810_23812_bundle_archive.zip -d path/to/where

They will receive several directories with data:
train - training dataset
test - dataset for test
val - dataset for checking results during training

Description:

The architecture of the neural network is presented in the form:
- input layer
- first convolutional layer
- first pooling layer
- second convolutional layer
- second pooling layer
- first fully connected layer
- second fully connected layer and a multi-variable layer

![CNN](image_project/CNN.PNG)

We train models on 20 eras, data is generated on the basis of batches for efficiency.
After training the model, we obtain the average value of losses (using cross_entropy_loss).

![train_model](image_project/train_model.PNG)

The results show that the proportion of correct answers of the model relative to the initial sample (accuracy) is 100% (on the train set) and 86% on the set (test):

![train_acc](image_project/train_acc.PNG)

Healthy lung example:

![Healthy](val/NORMAL/NORMAL2-IM-1427-0001.jpeg)

An example of an infected person's lungs:

![infected](val/PNEUMONIA/person1954_bacteria_4886.jpeg)


As a result, the model classifies accurately enough, to improve the results, you can use regularization to fine-tune the critical values of weights during training.

![result](image_project/result.PNG)
