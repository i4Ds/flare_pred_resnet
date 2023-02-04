# Solar flare prediction using multiple SDO channels
 Authors: Yana Shtyk, Olga Taran, André Csillaghy, Jonathan Donzallaz
 
 
Solar flare prediction is a major topic in space weather forecasting. In the last decade, this problem attracted an increased research interest due to the availability of large amounts of observational data as well as promising achievements in the field of machine learning. Deep learning is actively used in the recent state-of-the-art solar flare prediction approaches. However, the majority of previous attempts are based only on SDO/HMI magnetograms, while the capabilities of SDO/AIA data channels have been less studied. In this work, we aim at investigating the predictive capabilities of the SDO/AIA channels, individually as well as combined, along with the "traditional" HMI channels. More particularly, we focus on the data available in the SDOBenchmark data set that consists of SDO images of active regions, cropped from the full-sun originals. Using the multi-channel nature of the SDOBenchmark data set, we propose and analyse (i) a single model framework trained independently on the different data channels, (ii) a multi models framework with outputs aggregation that combines different data channels, and (iii) a single model framework with inputs aggregation that also combines the different data channels. All proposed frameworks make the binary prediction for $\ge$ C1.0-class within the following 24 hours. The obtained results show that, without a doubt, the HMI magnetogram give the highest true skill score. Nevertheless, the single model framew trained additionally on the AIA 94 and 193 channels outperform many relevant state-of-the-art approaches. Moreover, the joint use of different data channels in  the multi models framework with outputs aggregation allows to improve the best true skill score achieved by the HMI magnetograms alone. 

### How to run training process

#### Training the frameworks on the one or multiple SDO channels


Create cofiguration file \<filename\>.yaml with needed settings in the config/experiment folder and then run:
 ```
python solarnet/main.py --config_path "<config_path>/<filename>.yaml" --task "train"

```
 
### How to run testing process
 
#### Testing performance  of single model framework 


 
 ```
 python solarnet/main.py --config_path "<config_path>/<filename>.yaml" --task "test"
 ```
 
 #### Testing performance of multi models framework
 
 
Create cofiguration file \<filename\>.yaml in the config/experiment folder with needed settings and paths to the models to be tested and then run:
 
 ```
 python solarnet/main.py --config_path "<config_path>/<filename>.yaml" --task "test_multi"
 ```
 
 Type of aggregation should be specified in the configuration file
 
 ### Reproducibility of the results
 Pretrained weights of the models can be downladed from [here](https://drive.google.com/drive/u/0/folders/1BVJRjiCydCIi-oLCZsBIOWrVNnzagmz2). They can be used to reproduce the results.
 
 
 
 
 
 
 
 
 
