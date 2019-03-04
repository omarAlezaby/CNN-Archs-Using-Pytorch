# CNN architectures Using Pytorch
A try to impliment some of CNN common architectures using pytorch 

- Dataset used: CIFAR10.

# Training Notes. 

- Num of training epochs : 100 epoch.

- Training Time : 3 minutes/epoch.

# Accurcy: 
- VGG16 Arch without FC layers : 

    Val_acc : 83 , Tr_acc : 100 , Overfitting 

- VGG16 Arch With one FC(100) layer and without any Regulization: 

    Val_acc : 88.7 , Tr_acc : 99 , Overfitting 

- VGG16 Arch With one FC(100) layer, L2 Regulization(1e-5), dropout(.5) for FC layer and data augmentation : 

    Val_acc : 90 , Tr_acc : 97.6 , Overfitting 

- VGG16 Arch With one FC(100) layer, L2 Regulization(1e-5), dropout for all Conv layers, dropout(.5) for FC layer and data augmentation : 

    Val_acc : 88 , Tr_acc : 88 , No Overfitting 

- VGG16 Arch With one FC(100) layer, L2 Regulization(1e-5), dropout for each Conv group(after the pooling), dropout(.5) for FC layer and data augmentation : 

    Val_acc : 88 , Tr_acc : 93 , Overfitting, converge much faster, Plateau at epoch 32.
    
- VGG16 Arch With one FC(100) layer, L2 Regulization(1e-4), dropout for each Conv group(after the pooling), dropout(.5) for FC layer and data augmentation : 

    Val_acc : 89 , Tr_acc : 89 ,No Overfitting.



# References: 

[1] Karen Simonyan and Andrew Zisserman. Very deep convolutional networks for large-scale image recognition. arXiv preprint arXiv:1409.1556, 2014.

[2] Shuying Liu and Weihong Deng. Very deep convolutional neural network based image classifi- cation using small training sample size. In Pattern Recognition (ACPR), 2015 3rd IAPR Asian Conference on, pages 730–734. IEEE, 2015.
