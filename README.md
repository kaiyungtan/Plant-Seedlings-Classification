# Plant Seedlings Classification

### Data Description: 
You are provided with a training set and a test set of images of plant seedlings at various stages of grown. Each image has a filename that is its unique id. 

The dataset comprises 12 plant species.

The goal of the competition is to create a classifier capable of determining a plant's species from a photo.

Dataset: The project is from a dataset from Kaggle. 

Link to the Kaggle project site:https://www.kaggle.com/c/plant-seedlings-classification/data

### Steps 

1. Import the libraries, load dataset, print shape of data, visualize the images in dataset.  
2. Data Pre-processing:  
  a. Normalization.
  b. Gaussian Blurring.
  c. Masking
  d. Visualize data after pre-processing.
3. Make data compatible:  
  a. Split the dataset into training, testing, and validation set.
  b. Reshape data into shapes compatible with Keras models.
  c. Convert labels from digits to one hot vectors.
  d. Print the label for y_train[0].
4. Building CNN:  
  a. Define layers.
  b. Set optimizer and loss function. (Use Adam optimizer and categorical crossentropy.)
  5. Fit and evaluate model and print confusion matrix.  
6. Submit predictions on the test image on Kaggle. 


### CNN Model 1

*   2 convolution layers ( filters=64 / 128 , kernel_size=(3, 3) activation='relu')
*   MaxPool2D((2, 2)
*   Dropout(0.25)
*   Flatten
*   2 dense layers (128 / 64, activation='relu')
*   Dropout(0.25)
*   loss='categorical_crossentropy', optimizer='adam'
*   epoch = 200

Model 1 has 86% on training accuracy and 84 % on testing accuracy.

### CNN Model 2 

*   3 convolution layers (filters=64/128/128 , kernel_size=(3, 3) activation='relu')
*   MaxPool2D((2, 2),
*   Dropout(0.25)
*   Flatten
*   1 dense layer (256, activation='relu')
*   Dropout(0.5)
*   loss='categorical_crossentropy', optimizer='adam'
*   epoch = 200

Model 2 has 90% on training accuracy and 87 % on testing accuracy.

### CNN Model 3 - VGG16
*   Flatten
*   2 dense layers (256, activation='relu')
*   Dropout(0.5)
*   loss='categorical_crossentropy', optimizer='adam'
*   epoch = 200

Model 3 has 88.7% on training accuracy and 85.5% on testing accuracy.


### CNN Model 4 - InceptionV3

*   Flatten
*   2 dense layers (1024, activation='relu')
*   Dropout(0.5)
*   loss='categorical_crossentropy', optimizer='adam'
*   epoch = 200

Model 4 has 90% on training accuracy and 84% on testing accuracy.


### CNN Model 5

*   4 convolution layers (filters=64/64/128/256, kernel_size=(3, 3) activation='relu')
*   MaxPool2D((2, 2) 
*   Dropout(0.25)
*   GlobalMaxPool2D
*   Flatten
*   2 dense layers (256 / 256, activation='relu')
*   Dropout(0.25)
*   loss='categorical_crossentropy', optimizer='adam'
*   epoch = 200

Model 5 has 95% on training accuracy and 93% on testing accuracy.


# CNN Model 6 

*   6 convolution layers (filters=64/64/128/128/256/256, kernel_size=(3, 3) activation='relu')
*   MaxPool2D((2, 2) 
*   Dropout(0.25)
*   GlobalMaxPool2D
*   Flatten
*   3 dense layers (256/256/256, activation='relu')
*   Dropout(0.25)
*   loss='categorical_crossentropy', optimizer='adam'
*   epoch = 200

Model 6 has 90% on training accuracy and 88% on testing accuracy.

### Plant seedling visualization

![plant](https://user-images.githubusercontent.com/69633814/103784316-15dc0c80-503a-11eb-97e8-bf75467363ba.png)

### Plant seedling processed image
![image processed](https://user-images.githubusercontent.com/69633814/103784361-255b5580-503a-11eb-89f0-e6cea514fb9d.png)

### Model 5 graph - Accuracy over epochs for training and validation dataset
![graph](https://user-images.githubusercontent.com/69633814/103784385-2a200980-503a-11eb-9f78-787741d4e49f.png)

### Model 5 confusion matrix
![confusion matrix](https://user-images.githubusercontent.com/69633814/103784432-3ad07f80-503a-11eb-9080-9e51c8c64c3e.png)

### Model 5&6 submission result on Kaggle
![submission](https://user-images.githubusercontent.com/69633814/103784494-50de4000-503a-11eb-8ab6-66a1b577784e.png)

