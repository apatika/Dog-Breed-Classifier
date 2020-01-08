# Dog-Breed-Classifier
Estimating dog’s breed with Convolutional Neural Networks

## CNN to Classify Dog Breeds from Scratch

All images have been resized to 224 because most of the pretrained models require the input to be 224x224 images (224,224,3), the dataset is been augmentated by flipping and rotating randomly.

Fisrt I had included 3 convolutional layers with 16, 32 and 64 filters and 2 lineal layers but I could not get an accuracy more than 8%.

I finished with 4 convolutional and 3 linear layers increasing the parameters numbers in each layer to grap better the images details.

Every convolutional output is being pooled with a (2,2) factor and using dropout to avoid overfitting.

The last linear layer try to reduce the output to the 133 dog breeds classes.

I have found that the trainning process seems not to be not very efficient. I have tried adding additional layers, changing optimizers like Adam one and learning rates but I did not get a substantial improvement.

## CNN to Classify Dog Breeds Using Transfer Learning

* I have choosen to use the vgg19 model to apply for this problem, because it has been trained on more than a million images from the ImageNet database.
* I have only changed the out feature of the lasts linears layers and re-training the whole classifier section of the network.
* It seems to have a good performance.
