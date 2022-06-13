<img src= "images/clusters.png" width="930" height="200">

# Clustering Cryptos with Unsupervised Learning

This notebook analyzes cryptocurrency data, specifically changes in prices over various time intervals for various cryptocurrencies, and then clusters each cryptocurrency accordingly. 

This code takes two approaches to clustering: (1) using the elbow plot method to determine the optimal value of 'k' and then using the K-Means algorithm on the original (scaled) dataset to cluster, and (2) using the Principal Component Analysis (PCA) reduction technique followed by the elbow method for determing 'k', and then using the K-Means algorithm on the PCA-reduced dataset to cluster.

---
## Technologies

This application leverages python 3.7 with the following packages:

* pandas: an open-source library that offers easy-to-use data analysis tools for Python.
* pathlib: for creation of file paths allowing the application to interact with a computer's filesystem.
* hvplot.pandas: a visualization library included in the PyViz package that can produce advanced charts    
  and interactive visualizations. 
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

After importing the data (provided in a CSV file stored in the Resources folder of this repo), the data is prepared using the sklearn StandardScaler() function.

Next, the best value for 'k' is determined using the elbow plot method. Using this 'k' value, the K-Means algorithm is run in order to cluster the cryptocurrencies according to the price changes of cryptocurrencies provided.

The process detailed in the paragraph directly above is then repeated but this time using PCA to find the optimal clusters.

Finally, the two approaches are visually compared using overlay hvplots.

![ClusterApproachesCompared.](images/overlay.png)

---
## Contributors

Nicole Roberts,
elle.nicole.roberts@gmail.com

---

## License

[BSD 3](https://choosealicense.com/licenses/bsd-3-clause-clear/): BSD 3-clause is a permissive licence, allowing nearly unlimited freedom with the software as long as BSD copyright and license notice is included.