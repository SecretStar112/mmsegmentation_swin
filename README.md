# Swin Transformer For Semantic Segmentation Of Human Body Images
This repo contains the supported code and configurations to reproduce Swin Transformer for semantic segmentation.
## Goal
The goal is to do semantic segmentation on photos that can include one or more person. 
## Dataset source
The dataset is available on download [here](https://www.kaggle.com/datasets/tapakah68/segmentation-full-body-tiktok-dancing-dataset)
## Dataset preparation
In order to create labeled data I converted masks to label format [0,1].  
The file structure of the dataset is shown below:
```none
├── data
│   ├── full_body_tik_tok
│   │   ├── annotations
│   │   │   ├── training_1D
│   │   │   │   ├── xxx.png
│   │   │   │   ├── yyy.png
│   │   │   │   ├── zzz.png
│   │   │   ├── validation_1D
│   │   ├── images
│   │   │   ├── training
│   │   │   │   ├── xxx.png
│   │   │   │   ├── yyy.png
│   │   │   │   ├── zzz.png
│   │   │   ├── validation

```

# Installation
See <a href="https://github.com/Slava-git/mmsegmentation_swin/blob/master/docs/en/get_started.md"> get started</a> for installation

# Train and test
Navigate to <a href="https://github.com/Slava-git/mmsegmentation_swin/blob/master/Swin_Segmentation.ipynb"> train and test in colab</a>  
Notes:
* Refer to <a href="https://github.com/Slava-git/mmsegmentation_swin/blob/master/docs/en/tutorials/config.md"> config</a> to see example  
* Refer to <a href="https://github.com/Slava-git/mmsegmentation_swin/blob/master/docs/en/tutorials/customize_datasets.md"> custom dataset preparation</a>  
* Refer to <a href="https://github.com/Slava-git/mmsegmentation_swin/blob/master/docs/en/tutorials/customize_models.md"> custom model preparation</a>

# Web application
Navigate to <a href="https://github.com/Slava-git/mmsegmentation_swin/blob/master/Flask_app.ipynb"> flask app</a> to make prediction in web  
Note:
* Do not forget put your ngrok token

# Results
Refer to [youtube](https://youtu.be/XwDpAf7UP_4).

| Name                           | mAcc          |mIoU           | Model                                                                                        |
| -------------                  |:-------------:|:-------------:| -----:                                                                                       |
| swin_tiny_patch4_window7_224   | 0.9291        | 0.7851        | [model](https://drive.google.com/file/d/1-Qn7ksEGIn9nDqjWNRIu36U36MLPMjaE/view?usp=sharing)  |
| swin_base_patch4_window7_224   | 0.9015        | 0.7319        | [model](https://drive.google.com/file/d/1-D-lRnTU1X9QvlgDDwXZXYWlz3z4ipBZ/view?usp=sharing)  |
| fcn_r101_d8                    | 0.9798        | 0.9009        | [model](https://drive.google.com/file/d/1-UNojbH90Er29AfRZ9nkwCmA_x3gZPIo/view?usp=sharing)  |
| pspnet_r50-d8                  | 0.9611        | 0.9356        | [model](https://drive.google.com/file/d/1-FDtI81kBM3uEoSLFWr4LzgwQuWZTUuB/view?usp=sharing)  |
