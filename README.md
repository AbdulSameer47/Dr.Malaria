# Dr.Malaria
Using deep learning, foldscope and mobile based application for detecting malaria parasite

# PROPOSED MODEL 
 
 As shown in Fig 3. The image will enter the ResNet50 layer with the pretrained weights and the last layer is a classic fully connected dense layer with SoftMax activation. As shown in Fig.4 the proposed model consists of 2 layers, Pre- trained ResNet layer, flatten layer, dense layer with 512 units ,dropout layer with 30% drop out  and final dense layer (output layer with 2 units). Pre-Trained Weights for the ResNet50 model are to be imported. The input data will be trained with the pre-trained weights and the only layer which is learning with back propagation is the dense layer. Few layers such as Batch Normalization (BN) layers shouldn’t be frozen because the mean and variance of the dataset will be hardly matching the mean or variance from pre-trained weights. So, auto-tuning is adapted for the BN layers in ResNet50, i.e. few of the layers which are in the top  of ResNet50 shouldn’t be frozen. SoftMax is good for multi- class classification. We can also use sigmoid activation which is better than SoftMax for  binary classification. 
 
  
![Proposed Model](proposedmodel.JPG)
Fig -3: Proposed Architecture 
