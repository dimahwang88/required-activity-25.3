# Datasheet Template

As far as you can, complete the model datasheet. If you have got the data from the internet, you may not have all the information you need, but make sure you include all the information you do have. 

## Motivation

- For what purpose was the dataset created? 
- Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)? Who funded the creation of the dataset?

Traditional cell nucleus detection relies on pathologists with microscopes, which is a tedious, costly and time consuming progress. We develop a deep learning and stochastic processing method to auto-segment those microscopy images, named as Quick-in-process(Qip)-Net. Qip-Net was proposed as an automated method to detect cell nucleus under various conditions, such as randomized cell types, different magnifications, and varying image backgrounds. The network is constructed based on regions with convolution neural network features (RCNN). It is trained by 663 original images and their corresponding masks from Kaggle website. The results showed that Qip-Net could rapidly segment the cell nuclei from the testing dataset of complex and disruptive surroundings with better S-2 score around 3% compared to U-Net.
 
## Composition

- What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)? 
- How many instances of each type are there? 
- Is there any missing data?
- Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by    doctor–patient confidentiality, data that includes the content of individuals’ non-public communications)?


This dataset contains a large number of segmented nuclei images. The images were acquired under a variety of conditions and vary in the cell type, magnification, and imaging modality (brightfield vs. fluorescence). The dataset is designed to challenge an algorithm's ability to generalize across these variations.

Each image is represented by an associated ImageId. Files belonging to an image are contained in a folder with this ImageId. Within this folder are two subfolders:

images contains the image file.
masks contains the segmented masks of each nucleus. This folder is only included in the training set. Each mask contains one nucleus. Masks are not allowed to overlap (no pixel belongs to two masks).
The second stage dataset will contain images from unseen experimental conditions. To deter hand labeling, it will also contain images that are ignored in scoring. The metric used to score this competition requires that your submissions are in run-length encoded format. Please see the evaluation page for details.

As with any human-annotated dataset, you may find various forms of errors in the data. You may manually correct errors you find in the training set. The dataset will not be updated/re-released unless it is determined that there are a large number of systematic errors. The masks of the stage 1 test set will be released with the release of the stage 2 test set.

In addition to the images there is an accompanying collection of annotations. The annotations were originally created by the Broad Imaging Platform. The annotations take the form of a collection of masks for each image of nuclei. Each mask is a PNG file that contains the segmentation of exactly one nucleus in a folder with the same name as the image it refers to. Like the masks, the images of nuclei are also PNG.

The ground truth and annotations were originally created by the Broad Imaging Platform using a combination of GIMP and a web-based annotation tool created internally.


## Collection process

- How was the data acquired? 
- If the data is a sample of a larger subset, what was the sampling strategy? 
- Over what time frame was the data collected?


## Preprocessing/cleaning/labelling

- Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)? If so, please provide a description. If not, you may skip the remaining questions in this section. 
- Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)? 
 
## Uses

- What other tasks could the dataset be used for? 
- Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses? For example, is there anything that a dataset consumer might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g., stereotyping, quality of service issues) or other risks or harms (e.g., legal risks, financial harms)? If so, please provide a description. Is there anything a dataset consumer could do to mitigate these risks or harms? 
- Are there tasks for which the dataset should not be used? If so, please provide a description.

## Distribution

- How has the dataset already been distributed? 
- Is it subject to any copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?  

## Maintenance

- Who maintains the dataset?

Contributors
Riki Eggert, King's College London
Donna McPhie, McLean Hospital
Andrew Bradley and Gustavo Carneiro
Mariko Taga, Columbia University
Matthew Stachler, Brigham and Women's Hospital
Chris Lee, MIT
Alexander Chamessian, Ji Lab, Duke University
Florian Barthelemy, Miceli Lab, Center for Duchenne muscular dystrophy, UCLA
Lorraine Montel, Ecole Normale Superieure
Glyn Nelson, Newcastle University
Tim Becker, Fraunhofer EMB
Maria Frias, Foster Lab, Hunter College
Philipp Keller
Christian Marinaccio, Northwestern University
Vasiliy Chernyshev, Skoltech
several biologists who wished to remain anonymous
And of course, the Carpenter lab, Broad Institute

