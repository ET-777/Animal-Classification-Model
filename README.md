Animal Image Classification with CNN
-----------------------

Predict, out of 10 animal classes, to which class an animal image belongs to. The images are of medium quality and the model uses convolutional neural networks. Dataset is [here](https://www.kaggle.com/datasets/alessiocorrado99/animals10).

Installation
----------------------

### Download the data

* Clone this repo to your computer.
* Create a 'Data' folder in the project directory
* Create a 'train' and 'test' folder in the 'data' directory
* Download the data files from Kaggle into the `Data` folder.  
    * You can find the data [here](https://www.kaggle.com/datasets/alessiocorrado99/animals10).
    * You'll need to register with Kaggle to download the data.
* Extract the `.zip` file you downloaded into the 'train' folder.
* Download an image or several of one of the animal classes from a search engine into the 'test' folder.

### Install the requirements
 
* Install the requirements with 'anaconda' or with pip using `pip install -r requirements.txt`.
    * Make sure you use Python 3.
    * You may want to use a virtual environment for this.

Usage
-----------------------

* Open 'AnimalClassification.ipynb' with 'Jupyter Notebook'.
* Run the notebook
    * Make sure you are using 'tensorflow' with a 'GPU'.