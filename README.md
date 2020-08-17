# Dr.Malaria
Using deep learning, foldscope and mobile based application for detecting malaria parasite

# Demo



# PROPOSED MODEL 
 
 As shown in Fig 3. The image will enter the ResNet50 layer with the pretrained weights and the last layer is a classic fully connected dense layer with SoftMax activation. As shown in Fig.4 the proposed model consists of 2 layers, Pre- trained ResNet layer, flatten layer, dense layer with 512 units ,dropout layer with 30% drop out  and final dense layer (output layer with 2 units). Pre-Trained Weights for the ResNet50 model are to be imported. The input data will be trained with the pre-trained weights and the only layer which is learning with back propagation is the dense layer. Few layers such as Batch Normalization (BN) layers shouldn’t be frozen because the mean and variance of the dataset will be hardly matching the mean or variance from pre-trained weights. So, auto-tuning is adapted for the BN layers in ResNet50, i.e. few of the layers which are in the top  of ResNet50 shouldn’t be frozen. SoftMax is good for multi- class classification. We can also use sigmoid activation which is better than SoftMax for  binary classification. 
 
  
![](https://github.com/AbdulSameer47/Dr.Malaria/blob/master/proposedmodel.jpg)



#	Training the model 
 
Neural network learns through back propagation. Top layers in the ResNet50 aren’t frozen, i.e. those top layers learn through back propagation whereas other layers of ResNet50 are frozen. The weights getting updated during back-propagation is called fine-tuning [15]. Fine-tuning of the top layers in the ResNet50 should be done because there is no guarantee that the mean and variance of those layers will be similar to the mean and variance of our dataset.  
 
  ![](https://github.com/AbdulSameer47/Dr.Malaria/blob/master/summary.jpg)
 

# IMPLEMENTATION 
 
First take the blood sample from the patient on slide and place it under the foldscope. then launch the dr.malaria application and place the camera on the eyepiece of the foldscope such that microscopic image is clearly visible on the mobile screen then capture the image and press diagnose button which will predict whether the blood sample is infected or not infected as shown in Fig-6.

![](https://github.com/AbdulSameer47/Dr.Malaria/blob/master/architecture.jpg)
