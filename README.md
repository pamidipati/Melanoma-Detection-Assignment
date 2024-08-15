# Melanoma-Detection-Assignment
> Building a multiclass classification model using a custom convolutional neural network in TensorFlow which can accurately detect melanoma.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
### About Melanoma
- Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.
### About Dataset
- The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.
- The data set contains the following diseases:
Actinic keratosis
Basal cell carcinoma
Dermatofibroma
Melanoma
Nevus
Pigmented benign keratosis
Seborrheic keratosis
Squamous cell carcinoma
Vascular lesion

### About Project Pipeline
Data Reading/Data Understanding → Defining the path for train and test images 
Dataset Creation→ Create train & validation dataset from the train directory with a batch size of 32. Also, make sure you resize your images to 180*180.
Dataset visualisation → Create a code to visualize one instance of all the nine classes present in the dataset 
Model Building & training : 
Its a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescale images to normalize pixel values between (0,1).
Choosen an appropriate optimiser and loss function for model training
The model is trained for ~20 epochs

### Approach
- First model not having any dropouts and regularizations, it given decent accuracy but overfitting is observed
- Second Model has dropouts and regularizations that resolved overfitting issues but the accuracy is reduced.
- In the third model, Augumentor pipeline is used to balance the images count in every subset of image class, and considered dropout as well.This model resolved overfitting issue and accuracy improved as well.This model used 30 epochs.



## Conclusions
### First Model Findings (Without dropout)
- Trining Accuracy: 66.89% -> Model is performing reasonably well on the training data.however, improvement can be done.
- Validation Accuracy: 57.94% -> Model is not up to the mark on validation set compare to training set.This is case of overfitting.
- Trining Loss: 0.8864 -> More improvement can be done.
- Validation Loss: 2.1172 -> Overfitting is observed.

### Second Model Findings (Dropout and Regularization techniques used)
- Trining Accuracy: 49.77% -> Model is performing reasonably well on the training data.however, improvement can be done.
- Validation Accuracy: 47.65% -> Both validation accuracy and trainning accuracy are very much close, so this is perfectly fine.
- Trining Loss: 1.48 -> More improvement can be done.
- Validation Loss: 1.53 -> no overfitting but accuracy to be improved.

### Third Model Findings (Class Imbalancing is done using augumentor pipeline)
#### Without Dropout and Regularizations
- Trining Accuracy: 84.35% -> Model is performing reasonably well on the training data.No improvement is required.
- Validation Accuracy: 64.86% ->  Model is not up to the mark on validation set compare to training set.This is case of overfitting.
- Trining Loss: 0.4183 -> Its perfectly alright.
- Validation Loss: 1.33 -> Overfitting is observed.
#### With Only Dropout (No Reguarization)
- Trining Accuracy: 79.08% -> Model is performing reasonably well on the training data.No improvement is required.
- Validation Accuracy: 65.22% ->  Model is not up to the mark on validation set compare to training set.This is case of overfitting.
- Trining Loss: 0.58 -> Its perfectly alright.
- Validation Loss: 1.20 -> Overfitting is observed.(Dropuout alone not sufficient).
#### With Dropuout and Regularization
- Accuracy reached above 60%.
- No overfitting and UNderfitting.



## Technologies Used
Folowing libraries are used
- tensorflow
- keras
- numpy
- pandas
- matplotlib
- pathlib
- os
- PIL





## Contact
Created by [@pamidipati] - feel free to contact me!


