# Model Card

See the [example Google model cards](https://modelcards.withgoogle.com/model-reports) for inspiration. 

## Model Description

U-net architecture (example for 32x32 pixels in the lowest resolution). Each blue box corresponds to a multi-channel feature map. The number of channels is denoted on top of the box. The x-y-size is provided at the lower left edge of the box. White boxes represent copied feature maps. The arrows denote the different operations.

**Input:** Describe the inputs of your model 

128x128 image

**Output:** Describe the output(s) of your model

128x128 segmentation mask

**Model Architecture:** Describe the model architecture you’ve used

UNet is a fully convolutional network(FCN) that does image segmentation. Its goal is to predict each pixel's class. It is built upon the FCN and modified in a way that it yields better segmentation in medical imaging.

## Performance

The performance is evaluated by computing IoU betwee ground truth mask and predicted mask.

## Limitations

Outline the limitations of your model.

## Trade-offs

Outline any trade-offs of your model, such as any circumstances where the model exhibits performance issues. 
