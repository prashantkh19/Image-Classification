# Image-Scene-Classification

[fastai](https://docs.fast.ai/) framework is used to classify natural scenes images, provided in the [dataset](https://www.kaggle.com/puneet6060/intel-image-classification). 
Particularly, transfer learning on resnet-34 and resnet-50 models (trained on [Image-Net](http://image-net.org/)) is used.

## About Dataset

### Context
This is image data of Natural Scenes around the world.

### Content
This Data contains around 25k images of size 150x150 distributed under 6 categories. {'buildings' -> 0, 'forest' -> 1, 'glacier' -> 2, 'mountain' -> 3, 'sea' -> 4, 'street' -> 5 }

The Train, Test and Prediction data is separated in each zip files. There are around 14k images in Train, 3k in Test and 7k in Prediction. This data was initially published on [https://datahack.analyticsvidhya.com](https://datahack.analyticsvidhya.com) by Intel to host a Image classification Challenge.

### Acknowledgements
Thanks to [https://datahack.analyticsvidhya.com](https://datahack.analyticsvidhya.com) for the challenge and Intel for the Data.

## Result and Analysis

###  ResNet-34

#### Training summary:
Unfreeze model is trained with a variable learning rate ranging from 1e-6 to 1e-4.
<p align="center">
<img src="https://user-images.githubusercontent.com/27685757/71081341-05e65600-21b5-11ea-8ab6-b81618565f71.png" />
</p>

##### <I>Got an accuracy of **93.02 %** with 4 training epochs.</I>

#### Confusion Matrix:
<p align="center">
<img src="https://user-images.githubusercontent.com/27685757/71081564-77260900-21b5-11ea-80c8-ce88cb5efb31.PNG" />
</p>

It shows the model is most confused with buildings and streets, which is reasonable to some extent as the street view can have buildings also.

###  ResNet-50

#### Training summary:
Unfreeze model is trained with a variable learning rate ranging from 1e-6 to 1e-4.
<p align="center">
<img src="https://user-images.githubusercontent.com/27685757/71081365-10085480-21b5-11ea-86a5-ba156f746ce1.png" />
</p>

##### <I>Got an accuracy of **93.40 %** with 4 training epochs.</I>

#### Confusion Matrix:
<p align="center">
<img src="https://user-images.githubusercontent.com/27685757/71081565-77be9f80-21b5-11ea-9ab0-356f1bf1cdf7.PNG" />
</p>

It also showed the same confusion as the previous model.

> **The notebook can be easily viewed [here](https://www.kaggle.com/prashantkh19/intel-image-classification-resnet-93-40).**
