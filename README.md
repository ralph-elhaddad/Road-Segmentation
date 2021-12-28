# Road Segmentation

Hello all!

This is a repo for image segmentation from satellite imaging for the course EPFL CS-433 Machine Learning - Project 2.


**` The team members `:** BouAkl Carl, El Haddad Ralph


**` Team name `:** Road Island

## Instructions
To run the codes, make sure you have the correct version of tensorflow, keras etc… All the requirements are found in the **` requirements.txt`:** file and can be installed by using the following:
~~~~shell
pip install -r requirements.txt
~~~~
Furthermore, make sure that you downloaded the weights from the google drive link inside the **`link_for_wights.txt`:** file. Put these weights in the main repository, not in any folder.
Furthermore, the folder structure is shown but the images are empty except for the initial datatset and the training set. This should be enough to run all applications.
## Summary
### There are 3 models in this repository.
* Logisitc regression
* FCN8
* U-Net

The models can be trained, saved and tested. The scripts are explained below
### Logistic Regression
run the function "run_logreg" in order to predict using Logsitic Regression on the test image of your choice.
### Augmentation
This script was made as a library to augment the images. All functions were tested but not all functions were used for the final model. They were kept in this file. 
### fcn8.py
The architecture of the fully convolutional network is found here.
### kfold_cross_validation.py
This script was used to obtain the mean and standard deviation of the results of the unet. It basically runs the training and testing codes 4 times and gives the average of the F1 score.
### load_images.py
This script loads all the images and their masks in the augmentation folder.
### load_images_random_split.py
This script load all the images and their masks in the augmentation folder, shuffles them and then randomly splits them based on the percentage of split given as input.
### test_fcn8.py
Tests the results of the fcn. It loads a model that is saved when training
### test_unet.py
Tests the results of the Unet. It loads a model that is saved when training
### run.py 
This loads the model found on google drive and runs it on the test set, then provides a csv file of the results. This script with this model were used for the AI-crowd submission (Submission #169642)
### unet_v2.py
This script contains the architecture of the U-Net. 
