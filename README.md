# Study of Cloud Microphysics using Data Aggregation & Prediction of Liquid Water Content using Machine Learning 
The aim of this project is to test the efficacy of standard Parameterizations put forth in literature, which are dependent, solely on bulk droplet properties and can be estimated purely through calculations. <br>
### Detection of Cloudbase
Cloud base is the lowest altitude at which a visible portion of cloud can be observed. For liquid clouds, it can be defined as the lowest altitude in a height column at which visible portion is observed. Cloud base can be directly detected by certain instruments such as a microwave radiometer, ceilometer, etc. However, during the absence of such instruments, it is imperative to be able to approximate the cloud base, in order to proceed with further analysis of the recorded data, to thereby determine the cloud microstructure. In this section, a searching methodology to detect cloud base was put forth, using the backscatter coefficient as the deciding variable. <br>
![Search](https://github.com/yashgokhale/CMU-MS-Research/blob/main/images/searching_algo.png) <br>
Results of the searching algorithm in cloudbase detection where then combined with the clustering. <br>
### Spatial-temporal clustering
In order to superimpose values from one instrument onto another instrument having a different resolution, a three step clustering process has been implemented. The process of converting a parameter from one resolution to another resolution, two data files, from two corresponding instruments are used simultaneously.
![Clustering](https://github.com/yashgokhale/CMU-MS-Research/blob/main/images/clustering.PNG) 
The automated Python program outputs the following:
![Python](https://github.com/yashgokhale/CMU-MS-Research/blob/main/images/program.PNG)
The framework outputs a single .csv file containing the required features at the cloud base. The only argument needed to be passed is the date on which the output file is required. Internally, the framework retrieves data from multiple files for multiple instruments, from the directed file path. <br>
### Decision Tree Algorithm
The data under consideration was the combination of samples collected on each of the six individual dates, as listed in Clustered Data Analysis section. LWC was predicted using five dependent variables as: updraft velocity, droplet reflectivity, CCN, CDNC (calculated using Pinsky’s parametrization) and temperature. Based on this input dataset, with an 80%-20% random train-test data split, the decision tree algorithm was used to predict LWC. GridSearchCV was used for the optimal hyperparameters. <br>
![DT](https://github.com/yashgokhale/CMU-MS-Research/blob/main/images/dt2.PNG)

