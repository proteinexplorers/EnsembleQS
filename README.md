**EnsemblQS: An Ensemble of SVM, DT, and NB models with hard voting classfier, capable of predicting quorum sensing peptides with 96% accuracy.**

Stacking or Stacked Generalization is an ensemble machine learning algorithm.

It uses a meta-learning algorithm to learn how to best combine the predictions from two or more base machine learning algorithms.

The benefit of stacking is that it can harness the capabilities of a range of well-performing models on a classification task and make predictions that have better performance than any single model in the ensemble. 

**Methodology**


![image](https://user-images.githubusercontent.com/42578590/142976497-27b1c510-d9b4-4f78-9a1a-17880435df4c.png)

**Features considered to develop EnsemblQS**


**Feature set 1:** Aminoacid composition (AAC), Dipeptide composition (DPC), Dipeptide Deviation from Expected Mean (DEM), and tripeptide composition (TPC).

**Feature set 2:** Grouped Aminoacid composition (GAAC), Grouped Dipeptide composition (GDPC), and Grouped tripeptide composition (GTPC)

**Feature set 3:** CTD (Composition, Transistion, and Distribution) based features.


**Feature set 3:** Conjoint Triad based features. 


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


