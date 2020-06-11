# CNN-Image-Classification-Pneumonia
Pneumonia Image Classification from https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia

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
