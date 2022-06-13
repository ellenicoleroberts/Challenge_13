<img src= "images/neural.png" width="930" height="200">

# Risk Management with Neural Nets

This Jupyter notebook creates a neural network model that predicts whether applicants will be successful if funded by a venture capital firm. 

Included in the "Resources" folder is a CSV file containing data for more than 34,000 organizations that have received funding from a venture capital firm (Alphabet Soup). This dataset includes a variety of information about each business, including whether or not it ultimately became successful. 

Using machine learning and neural networks, the included Jupyter notebook uses the features in the provided dataset to create a binary classifier model that will predict whether an applicant will become a successful business.

---
## Technologies

This application leverages python 3.7 with the following packages:

* pandas: an open-source library that offers easy-to-use data analysis tools for Python.
* pathlib: for creation of file paths allowing the application to interact with a computer's filesystem.
* sklearn: a Python library for machine learning and statistical modeling including tools for classification, regression, clustering and dimensionality reduction.
* tensorflow: end-to-end open-source platform for machine learning permitting code to be run across multiple platforms in a highly efficient way.
* keras: an abstraction layer on top of TensorFlow that provides a Python interface for artificial neural networks.

---
## Installation Guide

Begin by cloning the GitHub repo (the same repo that this README.md file is contained within) into your terminal. 

Then activate the correct environment by inputting the following command into your terminal:

`conda activate dev`

Within this environment, next install the above listed dependencies. To do so, in your terminal while in this same repo, enter `pip install -r requirements.txt`.

---
## Usage

The first part of this notebook pre-processes the data so that it can be compiled and used with a neural network model. This includes encoding the dataset’s categorical variables using OneHotEncoder and then breaking up the dataset into seperate features (X) and target (y) datasets. Note, the column “IS_SUCCESSFUL” from the preprocessed DataFrame is chosen as the target variable.  

Next, the features and target sets are split into training and testing datasets. The features are then scaled using scikit-learn’s StandardScaler().

Using TensorFlow, a binary classification deep neural network model is defined. This model uses the dataset’s features as the inputs to predict whether an Alphabet Soup–funded startup will be successful. The number of inputs, layers, and nodes in each layer are established, as well as the number of outputs.  

The architecture of the model is next compiled using the binary_crossentropy loss function, the adam optimizer, and the accuracy evaluation metric. The training dataset is then fit to it with 50 epochs. 

Working with this model as a baseline, modifications are then made to it in the interest of improving the model's accuracy. Two different alternate models are tested in comparison to the baseline model: (1) the activation function is changed from "relu" to "tahn", and (2) an additonal layer is added. These models are finally compared to the baseline model.

---
## Contributors

Nicole Roberts,
elle.nicole.roberts@gmail.com

---

## License

[BSD 3](https://choosealicense.com/licenses/bsd-3-clause-clear/): BSD 3-clause is a permissive licence, allowing nearly unlimited freedom with the software as long as BSD copyright and license notice is included.