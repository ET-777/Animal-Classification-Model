Animal Image Classification with a Convolutional Neural Network (CNN)
-----------------------

Deep network for animal image classification. This is a multiclass classification task: Out of 10 animal classes, it predicts to which of them an animal image belongs to. The network consists of several convolutional neural layers with normalized data. The animal images are 28k medium quality images taken from search engines. Dataset is [here](https://www.kaggle.com/datasets/alessiocorrado99/animals10). You can see the data processing, model, code, and full explanations in the `AnimalClassification.ipynb` notebook above.

Quick Overview
----------------------

<p align="center">
<br />
Animal Classes
<br />
<br />
<img src="https://github.com/ET-777/Animal-Classification-Model/blob/main/images/classes.jpg" height="80%" width="80%"/>
<br />
<br />
</p>

To process the images, first they were resized to 80x80 pixels.

<p align="center">
<br />
Normal (scaled)
<br />
<img src="https://github.com/ET-777/Animal-Classification-Model/blob/main/images/normal.png"/>
<br />
<br />
Resized
<br />
<img src="https://github.com/ET-777/Animal-Classification-Model/blob/main/images/resized.png"/>
<br />
<br />
</p>

Then they were converted to numpy arrays which were in turn normalized by dividing the pixels by 255.

<p align="center">
<br />
<br />
Model
<br />
<img src="https://github.com/ET-777/Animal-Classification-Model/blob/main/images/model.jpg" height="50%" width="50%"/>
<br />
<br />
</p>

For the model, relu activations where used and the output layer has a linear activation with a SparseCategoricalCrossEntropy loss function, as it is better computiationally than a softmax activation.
The model was trained on 24 epochs with a validation split of 30% on the data.

To quickly test the model on a sample image, I used a picture of my dog and got a correct prediction.

<p align="center">
<br />
<br />
<img src="https://github.com/ET-777/Animal-Classification-Model/blob/main/images/dog.JPG" height="20%" width="20%"/>
<br />
<br />
<img src="https://github.com/ET-777/Animal-Classification-Model/blob/main/images/prediction.jpg"/>
<br />
<br />
</p>

Results
----------------------

<p align="center">
<br />
Training&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Validation
<br />
<img src="https://github.com/ET-777/Animal-Classification-Model/blob/main/images/graphs.png"/>
<br />
<br />
</p>

 Data | Loss | Accuracy
------------ | -------------|----
Training | 0.37 |0.87
Validation | 0.75 | 0.77


From the scores above, a decent model was trained. Further training would have resulted in overfitting the training data. To further improve the model, the image size could be increased.

Installation
----------------------

### Download the data

* Clone this repo to your computer.
* Create a `Data` folder in the project directory
* Create a `train` and `test` folder in the `Data` directory
* Download the data files from Kaggle into the `Data` folder.  
    * You can find the data [here](https://www.kaggle.com/datasets/alessiocorrado99/animals10).
    * You'll need to register with Kaggle to download the data.
* Extract the `.zip` file you downloaded into the `train` folder.
* Download an image or several of one of the animal classes from a search engine into the `test` folder.

### Install the requirements
 
* Install the requirements with `anaconda` or with pip using `pip install -r requirements.txt`.
    * Make sure you use Python 3.
    * You may want to use a virtual environment for this.

Usage
-----------------------

* Open `AnimalClassification.ipynb` with `Jupyter Notebook`.
* Run the notebook
    * Make sure you are running `tensorflow` with a `GPU`.
