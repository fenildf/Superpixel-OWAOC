# Superpixel-based online wagging one-class ensemble for feature selection in foreground/background separation

Last Page Update: **19/03/2018**


We present a novel online one-class ensemble based on wagging  to select suitable features to each region of a certain scene to distinguish the foreground objects from the background. In addition, we propose a mechanism to update the importance of each feature discarding insignificantly features over time. 

HIGHLIGHTS

* A novel methodology to select the best features based on wagging.
* A superpixel segmentation strategy to improve the segmentation performance, increasing the computational efficiency of our ensemble.
* A mechanism called Adaptive Importance Computation and Ensemble Pruning (AIC-EP) to suitably update the importance of each feature discarding insignificantly features over time.

BRIEF OVERVIEW OF THE PROPOSED FRAMEWORK
---------------------------------------------------
<p align="center"><img src="https://raw.githubusercontent.com/carolinepacheco/Superpixel-OWAOC/master/docs/ensemble_proposed2.png" border="0" /></p>

<center> <small> Brief overview of the proposed framework. A set of features are extracted from the training image sequence. Next, our wagging version creates different pools of IWOC-SVM classifiers from a certain feature. A heuristic approach called Small Votes Instance Selection (SVIS) is used in the IWOC-SVM model updating step. Finally, we use a mechanism called Adaptive Importance and Ensemble Pruning (AIC-EP) to update the importance of the classifiers discarding insignificantly classifiers over time. Only the classifiers with high importance are selected and combined to form a strong classifier. The whole framework described here works as incremental manner. </center>


ALGORITHM: THE WAGGING FOR FEATURE SELECTION 
---------------------------------------------------
<p align="center"><img src="https://raw.githubusercontent.com/carolinepacheco/Superpixel-OWAOC/master/docs/algorithm.png" border="0"/></p>


BACKGROUND SUBTRACTION RESULTS ON RGB-D DATASET​​​​​​​​​​​​​​
---------------------------------------------------
<p align="center"><img src="https://raw.githubusercontent.com/carolinepacheco/Superpixel-OWAOC/master/docs/rgbd_imp_features.png" border="0" /></p>
<center> <small> Background subtraction results on RGB-D dataset -- (a) original frame, (b) features map showing most important feature for each region and (c) its respective histogram of features importance.  </center>

Citation
--------
If you use this code for your publications, please cite it as:
```
@inproceedings{silva Caroline
author    = {Silva, Caroline and Bouwmans, Thierry and Frelicot, Carl},
title     = {Superpixel-based incremental wagging one-class ensemble for feature selection in foreground/background separation},
booktitle = {Pattern Recognition Letters (PRL)},
year      = {2017},
url       = hhttps://www.sciencedirect.com/science/article/pii/S0167865517304038}
```