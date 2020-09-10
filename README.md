# Covid-19-detection
Automated detection of COVID-19 cases using X-Ray images. <br /><br />

Used Transfer Learning to Classify the images of X-ray in three classes:-<br />
1. Covid-19 <br />
2. No-Finding<br />
3. Pneumonia<br /><br />

Dataset is the publicly available CoronaHack-Chest X-Ray-Dataset which can be downloaded from this link: https://www.kaggle.com/praveengovi/coronahack-chest-xraydataset. This dataset contains the following number of images: 125 COVID-19, 500 bacterial, and  500 viral pneumonias. <br /><br />

Splitted the data in three Train, Valid and Test part using Split-Folder python script.<br />
Split-Folder.ipynb uses (os) module to read all the images and split it in three different folder.<br /><br />

After that since we have a very small dataset<br />
We will perform Augmentation on the dataset using (ImageDataGenerator).<br /><br />

mageDataGenerator transforms and rotates our images to forms new images from<br />
Pre-existing images.<br />
This will generalise our dataset.<br /><br />

We will use the Resnet pre-trained model to perform transfer training on our model.<br />
Then we will build our model using Resnet pre-trained model.<br /><br />

hen we will set Loss function as Categorical Crossentropy.<br />
And Optimizers as Adam.<br /><br />

Then we will compile our model.<br /><br />

After compiling, we use ReduceLROnPlateau, which will reduce learning rate whenever our<br />
model stops improving any more.<br />
Reducing learning rate helps our model to even learn more from our data.<br /><br />

Finally, we will train our model on already split training and validation data.<br /><br />

After getting our model trained, we will plot our results.<br />
Training Accuracy vs Validation Accuracy<br />
Training Loss vs Validation Loss<br /><br />

After training <br />
We reached :- <br />
Training accuracy = 79.06%    <br />
Validation accuracy = 79.64%<br /><br />

The graph is shown below:-<br /><br />

<img src="https://github.com/gearhead0909/Covid-19/blob/master/Score.jpg" alt="alt text" width="500" height="300"><br /><br />

After that we will save our trained model.<br />
So that we can load it later and perform prediction.<br /><br />

After evaluating,<br />
We achieved of 74.63%
