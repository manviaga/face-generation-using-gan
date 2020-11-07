# face-generation-using-gan
This repo contains the code for DCGAN network that uses celebrity faces to train and then generates synthetic faces.
This is a project in Udacity's Deep LEarning Nano Degree Program. 

DCGAN consists of two networks - Discriminator and Generator. 
Model of Discriminator:  
layer1 :  Conv2d: 3->512, kernel size=4, stride =2, padding 1, bias=0  
layer2 :  Conv2d: 512->1024, kernel size=4, stride =2, padding 1, bias=0 -> batchnorm  
layer3 :  Conv2d: 1024->2048, kernel size=4, stride =2, padding 1, bias=0 -> batchnorm  
layer4 :  Linear: 32768->1, bias=1  

Model of Generator:  
Layer1:  Linear: 100->32768, bias=True) -> view 2048x4x4  
Layer2:  ConvTranspose2d: 2048->1024, kernel_size=4, stride=2, padding=1, bias=0) -> batchnorm  
layer3:  ConvTranspose2d: 1024->512, kernel_size=4, stride=2, padding=1), bias=0)-> batchnorm  
layer4:  ConvTranspose2d: 512->3, kernel_size=4, stride=2, padding=1, bias=0)  
