# Stochastic-Attentions-and-Context-Learning-for-Person-Re-id
Stochastic Attentions and Context Learning for person re-identification

# Person re-identification (re-id)
Person re-identification (re-id) identifies a query person in multiple non overlapping camera views where the same person appears in different poses, angles and views under different illumination conditions. Person re-identification is one of the major surveillance components that needs automation to ensure 24/7 public security. 

![alt text](https://github.com/naziaperwaiz/Stochastic-Attentions-and-Context-Learning-for-Person-Re-id/blob/main/Figures/re-id.jpg)

# Proposed architecture

![alt text](https://github.com/naziaperwaiz/Stochastic-Attentions-and-Context-Learning-for-Person-Re-id/blob/main/Figures/network.jpg)

The proposed work is based on deep-learning based person re-identification library "torchreid", written in pytorch. The detailed steps to install this library along with prerequisites are available at https://github.com/KaiyangZhou/deep-person-reid. The library provides a unified interface for training and testing of various person re-identification datasets.

# Training

The configuration file (config.py) sets person re-id dataset Market1501 as the default dataset. To choose any other person re-id dataset, Ln 18-19 needs to be changed in the config file for respective dataset (see torchreid/data/datasets/image). The code will automatically download and use the respective dataset when the training script is run. Moreover pretrained Imagenet weights are automatically downloaded and used for the training.

Training: Start the training by using command: python train.py

# Proposed results
The proposed network is trained and evaluated on four different preson re-id datasets, graphical representation of the results is given below:

![alt text](https://github.com/naziaperwaiz/Stochastic-Attentions-and-Context-Learning-for-Person-Re-id/blob/main/Figures/graphs.PNG)


![alt text](https://github.com/naziaperwaiz/Stochastic-Attentions-and-Context-Learning-for-Person-Re-id/blob/main/Figures/comparison%20with%20existing%20works.JPG)

The evaluation is automatically done after training of the model, however for early evaluation, evaluation frequency (Ln 103 of config file) should be changed (can be set as 10, 20 etc). For only evaluation using trained model weights, change the Ln 102 of config file by setting test.evaluate=True. Trained weights of the proposed model for Market1501 dataset are available at https://drive.google.com/drive/folders/1PxmG0Na_wwe1F_97QlNi9Eyc-RAJP5-T?usp=sharing.


If you find this code useful to your research, please cite the following papers.

@article{torchreid, title={Torchreid: A Library for Deep Learning Person Re-Identification in Pytorch}, author={Zhou, Kaiyang and Xiang, Tao}, journal={arXiv preprint arXiv:1910.10093}, year={2019} }
