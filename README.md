# Stochastic-Attentions-and-Context-Learning-for-Person-Re-id
Stochastic Attentions and Context Learning for person re-identification

# Person re-identification (re-id)
Person re-identification (re-id) identifies a query person in multiple non overlapping camera views where the same person appears in different poses, angles and views under different illumination conditions. Person re-identification is one of the major surveillance components that needs automation to ensure 24/7 public security. 

![alt text](https://github.com/naziaperwaiz/Stochastic-Attentions-and-Context-Learning-for-Person-Re-id/blob/main/Figures/re-id.jpg)

# Proposed architecture

The proposed solution learns the highly discriminative regions of pedestrian images along with focusing on the non-discriminative regions which provide sufficient contextual information to recognize a person with negligible additional computational resources.

![alt text](https://github.com/naziaperwaiz/Stochastic-Attentions-and-Context-Learning-for-Person-Re-id/blob/main/Figures/network.jpg)

The proposed work is based on deep-learning based person re-identification library "torchreid", written in pytorch. The detailed steps to install this library along with prerequisites are available [here](https://github.com/KaiyangZhou/deep-person-reid). The library provides a unified interface for training and testing of various person re-identification datasets.

# Datasets

If training script does not download the dataset, kindly download respective dataset from given links and place in the "/torchreid/data/" folder before starting the training.
## Market1501
Market 1501 dataset can be downloaded from [Openlink](http://zheng-lab.cecs.anu.edu.au/Project/project_reid.html)
## DukeMTMC-reID
DukeMTMC-reID dataset can be downloaded from [GoogleDrive](https://drive.google.com/u/1/uc?id=1jjE85dRCMOgRtvJ5RQV9-Afs-2_5dY3O&export=download)
## CUHK03
CUHK03 dataset can be downloaded from the [author's webpage](https://www.ee.cuhk.edu.hk/~xgwang/CUHK_identification.html). You need to fill in your details in the form after clicking the "Download" button. 
## MSMT17
MSMT17 dataset can be downloaded by following the detailed instructions available [here](https://www.pkuvmc.com/dataset.html)

# Training

The configuration file (config.py) sets person re-id dataset Market1501 as the default dataset. To choose any other person re-id dataset, Ln 18-19 needs to be changed in the config file for respective dataset (see torchreid/data/datasets/image). The code will automatically download and use the respective dataset when the training script is run. Moreover pretrained Imagenet weights are automatically downloaded and used for the training.

Training: Start the training by using command: python train.py

# Proposed results
The proposed network is trained and evaluated on four different preson re-id datasets, graphical representation of the results is given below:

![alt text](https://github.com/naziaperwaiz/Stochastic-Attentions-and-Context-Learning-for-Person-Re-id/blob/main/Figures/graph1.png)


![alt text](https://github.com/naziaperwaiz/Stochastic-Attentions-and-Context-Learning-for-Person-Re-id/blob/main/Figures/comparison%20with%20existing%20works.JPG)

The evaluation is automatically done after training of the model, however for early evaluation, evaluation frequency (Ln 103 of config file) should be changed (can be set as 10, 20 etc). For only evaluation using trained model weights, change the Ln 102 of config file by setting test.evaluate=True. Trained weights of the proposed model for Market1501 dataset are available at https://drive.google.com/drive/folders/1PxmG0Na_wwe1F_97QlNi9Eyc-RAJP5-T?usp=sharing.


If you find this code useful to your research, please cite the following papers.

@article{torchreid, title={Torchreid: A Library for Deep Learning Person Re-Identification in Pytorch}, author={Zhou, Kaiyang and Xiang, Tao}, journal={arXiv preprint arXiv:1910.10093}, year={2019} }
