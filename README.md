# Stochastic-Attentions-and-Context-Learning-for-Person-Re-id
Stochastic Attentions and Context Learning for person re-identification


The proposed work is based on deep-learning based person re-identification library "torchreid", written in pytorch. The detailed steps to install this library along with prerequisites are available at https://github.com/KaiyangZhou/deep-person-reid. The library provides a unified interface for training and testing of various person re-identification datasets.


The configuration file (config.py) sets person re-id dataset Market1501 as the default dataset. To choose any other person re-id dataset, Ln 18-19 needs to be changed in the config file for respective dataset (see torchreid/data/datasets/image). The code will automatically download and use the respective dataset when the training script is run. Moreover pretrained Imagenet weights are automatically downloaded and used for the training.

Training: Start the training by using command: python train.py

The evaluation is automatically done after training of the model, however for early evaluation, evaluation frequency (Ln 103 of config file) should be changed (can be set as 10, 20 etc). For only evaluation using trained model weights, change the Ln 102 of config file by setting test.evaluate=True. Trained weights of the proposed model for Market1501 dataset are available at https://drive.google.com/drive/folders/1PxmG0Na_wwe1F_97QlNi9Eyc-RAJP5-T?usp=sharing.

If you find this code useful to your research, please cite the following papers.

@article{torchreid, title={Torchreid: A Library for Deep Learning Person Re-Identification in Pytorch}, author={Zhou, Kaiyang and Xiang, Tao}, journal={arXiv preprint arXiv:1910.10093}, year={2019} }
