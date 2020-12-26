![LOGO](images/LOGO.png)



# **Architectural Basics**

This gives a description of the different techiniques used to obtain an accuracy of 99.4% on MNIST dataset using Convolutional Neural Networks with less than 15K parameters

## Iterations

Observations in each iteration were described below:



### First DNN

* A basic CNN pipeline is established. This is to ensure the code is executed successfully.

  

### Second DNN

* An eight layers CNN consisting of 3X3 Convolutions, 1x1 Convolutions and MaxPooling layers was built

* The number of layers were considered by taking into consideration the Receptive field

* Initially the total number of channels were chosen so that the number of parameters were less than 15K

* Validation check was included to understand the performance of the model during the training process

* The transition layer i.e. 1x1 Convolution with MaxPooling layer is added after 3 convolutions from the input

* The model training was executed for 10 epochs using the default learning rate and default optimiser i.e. Adam

* The validation accuracy was around 99.05 at last epoch. It was also observed that the validation accuracy reached to 99.07 during the training process i.e. during 10 epochs

* With the number of parameters around 14 K, it can be inferred that this architecture is a good starting point. Further improvements can be considered in subsequent steps

  

### Third DNN

* Batch Normalization layers were added after each Convolution layer

* A droput of 0.1 was also added after each Convolution and Batch Normalization layer

* Droput and Batch Normalization was not considered at the last Convolution layer i.e. the layer before Softmax

* The number of epochs for training were increased from 10 to 20

* The validation accuracy was around 99.25 at last epoch. It was also observed that the validation accuracy reached to 99.39 during the training process i.e. during 20 epochs

* With the number of parameters still being 14K and validation accuracy touching 99.39 during training, it can be inferred the target validation accuracy i.e. 99.4 can be achieved by this architecture with further improvements.

  

### Fourth DNN

* The architecture was updated by reducing the number of filters and moving the MaxPooling layer further away from the last layer
* A learning rate of 0.008 and batch size of 256 was considered with custom learning rate scheduler
* The training was carried for about 40 epochs
* With the number of parameters around 10.5 K, validation accuracy of about 99.41 was achieved at the last epoch. Highest validation accuracy of about 99.42 was achieved during the training process.
* Further improvements to learning rate and validation accuracy may help obtain validation accuracy of 99.4 in less number of epochs.



## Built With

* [Google Colab](https://colab.research.google.com/) - Colaboratory is a free Jupyter notebook environment that requires no setup and runs entirely in the cloud

* [Keras](https://colab.research.google.com/) - The Python Deep Learning library

  

