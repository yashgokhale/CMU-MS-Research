# Study of Cloud Microphysics using Data Aggregation & Prediction of Liquid Water Content using Machine Learning 
The aim of this project is to test the efficacy of standard Parameterizations put forth in literature, which are dependent, solely on bulk droplet properties and can be estimated purely through calculations. <br>
### Detection of Cloudbase
Cloud base is the lowest altitude at which a visible portion of cloud can be observed. For liquid clouds, it can be defined as the lowest altitude in a height column at which visible portion is observed. Cloud base can be directly detected by certain instruments such as a microwave radiometer, ceilometer, etc. However, during the absence of such instruments, it is imperative to be able to approximate the cloud base, in order to proceed with further analysis of the recorded data, to thereby determine the cloud microstructure. In this section, a searching methodology to detect cloud base was put forth, using the backscatter coefficient as the deciding variable. <br>
![Search](https://github.com/yashgokhale/CMU-MS-Research/blob/main/images/searching_algo.png) <br>
Results of the searching algorithm in cloudbase detection where then combined with the clustering. <br>
### Spatial-temporal clustering
In order to superimpose values from one instrument onto another instrument having a different resolution, a three step clustering process has been implemented. The process of converting a parameter from one resolution to another resolution, two data files, from two corresponding instruments are used simultaneously.
![Clustering](https://github.com/yashgokhale/CMU-MS-Research/blob/main/images/clustering.PNG) <br>
The automated Python program outputs the following:
![Python] (https://github.com/yashgokhale/CMU-MS-Research/blob/main/images/program.PNG) <br>

