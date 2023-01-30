# ResNet
 Authors: Yana Shtyk, Olga Taran, André Csillaghy, Jonathan Donzallaz
 
 
The work addresses the problem of prediction of solar flares. To research this problem a machine learning technique called recurrent neural network was used.
We trained and tested our model on the SDOBenchmark dataset.  It is a time series dataset created by FHNW. 
It consists  of images of active regions cropped from SDO data. 
As the dataset has 10 different SDO channels, we were able to investigate prediction capabilities of all of them. Best TSS of 0.64 was obtained using a magnetogram. Furthermore, we found out that channel aggregation can help to improve prediction capabilities of the model. Using this technique we managed to achieve TSS of 0.7.

### How to run training process

#### Training on the one or multiple channels


Create cofiguration file \<filename\>.yaml with needed settings in the config/experiment folder and then run:
 ```
python main.py --config_path "<config_path>/<filename>.yaml" --task "train"

```
 
### How to run testing process
 
#### Testing the model


 
 ```
 python main.py --config_path "<config_path>/<filename>.yaml" --task "test"
 ```
 
 #### Testing performance of the models with outputs aggregation
 
 
Create cofiguration file \<filename\>.yaml in the config/experiment folder with needed settings and paths to the models to be tested and then run:
 
 ```
 python main.py --config_path "<config_path>/<filename>.yaml" --task "test_multi"
 ```
 
 Type of aggregation should be specified in the config file
 
 ### Reproducibility of the results
 Pretrained weights of the models can be downladed from [here](https://drive.google.com/drive/u/0/folders/1BVJRjiCydCIi-oLCZsBIOWrVNnzagmz2). They can be used to reproduce the results.
 
 
 
 
 
 
 
 
 
