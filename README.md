# Segmentation of nuclei images.


## NON-TECHNICAL EXPLANATION OF YOUR PROJECT

Identifying the cells’ nuclei is the starting point for most analyses because most of the human body’s 30 trillion cells contain a nucleus full of DNA, the genetic code that programs each cell. Identifying nuclei allows researchers to identify each individual cell in a sample, and by measuring how cells react to various treatments, the researcher can understand the underlying biological processes at work.

## DATA
A summary of the data you’re using, remembering to include where you got it and any relevant citations. 


This dataset contains a large number of segmented nuclei images of size 128x128 pixels for both training images and masks. The images were acquired under a variety of conditions and vary in the cell type, magnification, and imaging modality (brightfield vs. fluorescence). The dataset is designed to challenge an algorithm's ability to generalize across these variations.

## MODEL 
A summary of the model you’re using and why you chose it. 

UNet is a fully convolutional network(FCN) that does image segmentation. Its goal is to predict each pixel's class. It is built upon the FCN and modified in a way that it yields better segmentation in medical imaging.

## HYPERPARAMETER OPTIMSATION
Description of which hyperparameters you have and how you chose to optimise them. 

Hyperparameter for U-Net training was done heuristically without applying Bayesian or other optimisation methods.

## RESULTS
A summary of your results and what you can learn from your model 

U-Net outputs 128x128 segmentation masks, we can compute the difference between ground truth and predicted masks using IoU metric.

You can include images of plots using the code below:
![Screenshot](image.png)

## (OPTIONAL: CONTACT DETAILS)
If you are planning on making your github repo public you may wish to include some contact information such as a link to your twitter or an email address. 

