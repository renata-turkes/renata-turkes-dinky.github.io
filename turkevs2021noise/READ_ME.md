Noise robustness of persistent homology on greyscale images, across filtrations and signatures  
Supplementary material  

Author: Renata Turkes  
<br>
<br>
<br>
The folder turkevs2021noise contains the code used for computational experiments on the MNIST 
dataset of handwritten digits in the aforementioned paper: <b>turkevs2021noise.ipynb</b>

The code allows to replicate our study, or to easily investigate the noise robustness of PH with 
different filtrations and persistence signatures, and their parameters and corresponding metric, 
for other datasets of greyscale images, types of noise and/or classifiers.
<br>
<br>
<br>
Since the runtime of some parts of the notebook is quite extensive, the folder also includes 
the most important variables from our experiment on 1000 MNIST images, in variables.zip. First of all, both non-noisy and noisy data is stored:
- data_trnsf.pkl: images
- data_filt_trnsf.pkl: filtration function values 
- data_sign_homdim_filt_trnsf.pkl: PH across persistence signatures, homological dimensions and filtrations  

To evaluate the stability of PH, the following variables are used:  
- dists_filt_trnsf_data_data.pkl: distance between filtration function values on the non-noisy and noisy images
- dists_sign_homdim_filt_trnsf_data_data.pkl: distance between PH on the non-noisy and noisy images  

To evaluate the noise robustness of PH features in a classification task, we rely on the classification accuracy
of SVM trained on non-noisy data, and then tested on non-noisy or noisy data:  
- svm_acc_data_filt_trnsf.pkl: SVM accuracy for filtration functions
- svm_acc_data_sign_homdim_filt_trnsf.pkl: SVM accuracy for PH  

Should one be interested to extract more information about the SVM performance, such as the confusion matrices,
the estimators themselves are also stored:  
- svm_classifier_data_filt.pkl: SVM classifier trained on filtration functions
- svm_classifier_data_sign_homdim_filt.pkl: SVM classifier trained on PH
