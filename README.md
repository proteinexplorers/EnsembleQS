**EnsemblQS: An Ensemble of SVM, DT, and NB models with hard voting classfier, capable of predicting quorum sensing peptides with 96% accuracy.**

Stacking or Stacked Generalization is an ensemble machine learning algorithm.

It uses a meta-learning algorithm to learn how to best combine the predictions from two or more base machine learning algorithms.

The benefit of stacking is that it can harness the capabilities of a range of well-performing models on a classification task and make predictions that have better performance than any single model in the ensemble. 


**Implemented in Scikit-learn Library.**


Scikit-learn is an open source machine learning library for Python. You have a number of options when it comes to installing scikit-learn, depending on your needs:

    If you don’t have Python installed, you can install scikit-learn as part of a Python distribution, such as ActivePython.
    If you already have Python and prefer to install pre-built binaries, you can install scikit-learn by simply running the following command:

    pip install scikit-learn

    Pre-built binaries may contain malicious code, especially if you mistakenly install a typo-squatted version. Instead, consider installing Python libraries from source code. The simplest way to build scikit-learn from source is to use the ActiveState Platform to automatically build and package it for Windows, Mac or Linux.


Scikit-Learn Step by Step Installation

For most users, the best approach is to install the binary version of scikit-learn using an official release from pypi.org, the Python Package Index. You can do so with the following steps:

1. Scikit-learn requires Python 3.6+. To check which version of Python you have installed, run the following command:

python3 --version

The output should be similar to:

Python 3.8.2

2. If you have a valid Python version you can run the following command to download and install a pre-built binary of scikit-learn:

pip install scikit-learn

The following dependencies will be automatically installed along with scikit-learn:

    NumPy 1.13.3+
    SciPy 0.19.1+
    Joblib 0.11+
    threadpoolctl 2.0.0+

Alternatively, if you already have scikit-learn and/or any of its dependencies are already installed, they can be updated as part of the installation by running the following command:

pip install -U scikit-learn

You can verify your Scikit-learn installation with the following command:

python -m pip show scikit-learn

The output should be similar to:

verify your Scikit-learn installation

If you want to create plots and charts based on the data you use in scikit-learn, you may also want to consider installing matplotlib. For information about matplotlib and how to install it, refer to ‘What is Matplotlib in Python’?
How to Import Scikit-Learn in Python

Once scikit-learn is installed, you can start working with it. A scikit-learn script begins by importing the scikit-learn library:

import sklearn

It’s not necessary to import all of the scitkit-learn library functions. Instead, import just the function(s) you need for your project. For example, to import the linear regression model, enter:

from sklearn import linear_model

Or try:

from sklearn.linear_model import LinearRegression


**Methodology**


![image](https://user-images.githubusercontent.com/42578590/142976497-27b1c510-d9b4-4f78-9a1a-17880435df4c.png)

**Features considered to develop EnsemblQS**


**Feature set 1:** Aminoacid composition (AAC), Dipeptide composition (DPC), Dipeptide Deviation from Expected Mean (DEM), and tripeptide composition (TPC).

**Feature set 2:** Grouped Aminoacid composition (GAAC), Grouped Dipeptide composition (GDPC), and Grouped tripeptide composition (GTPC)

**Feature set 3:** CTD (Composition, Transistion, and Distribution) based features.


**Feature set 4:** Conjoint Triad based features. 


**We recommend the users to use **ifeature package** for feature extraction.**

iFeature is a comprehensive Python-based toolkit for generating various numerical feature representation schemes from protein or peptide sequences. iFeature is capable of calculating and extracting a wide spectrum of 18 major sequence encoding schemes that encompass 53 different types of feature descriptors. 

**Python Package:** https://github.com/Superzchen/iFeature/



**Web server:** https://ifeature.erc.monash.edu/



**Result from ensemble model**


The accuracy of EnsemblQS is 8%, 8%, 3 %, 10%, and 7 % higher than those resulting from using the SVM, DT, RF, KNN, and GNB baseline models,thus highlighting the superiority of our proposed model. The comparisons to the previous works demonstrate that the EnsemblQS model performed better than the existing QS peptide prediction tools in terms of both MCC and accuracy. When evaluated on an independent dataset of 40 QSP peptides, the EnsemblQs showed 97% accuracy with MCC and auROC values of 0.91 and 0.94 respectively. 


**On the base of all the above efforts, we conclude that our EnsemblQS model adds some new contributions in the area of predicting QS peptides:**


• We demonstrated that increasing the heterogeneity of the input data positively influence the performance of both baseline models and EnsemblQS. We suggest the future works to increase the heterogeneity to the input data by considering widely diverse feature descriptors, instead of rely on simple composition based descriptors. 


• The Hyperparameter tuning improves the performance of baseline models. 


• To the best of our knowledge, we introduced the first stacked ensemble model namely EnsemblQS (SVM+DT+NB) to predict QS peptides, which provide higher accuracy (96%) and specifity (98%), compared to baseline models and existing state of art QS peptide predicting tools. 


