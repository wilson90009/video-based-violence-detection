# video-based-violence-detection
Final project of course "Introduction to Deep learning", CCU, Taiwan
# Code's reference

https://github.com/mchengny/RWF2000-Video-Database-for-Violence-Detection

# Preprocess Data

Remane folder RWF-2000 to RWF

Run notebook: Preprocessing.ipynb

# Re-implement original model: Paper's ACC 84.5, Our's: 84.25

Notebook: Original_Network.ipynb

# Enhance deep feature: Reduce number of conv3d and filter,  add more fully connected layers: ACC 86.5%

Notebook: Enhance_Deep_Feature.ipynb

Best weight (ACC 86.5% on val set): https://drive.google.com/file/d/11UvBe8ZJy09SkKu_d-hhp5XmEPdNMbve/view?usp=sharing

# Enhance deep feature (second): Reduce number of frame per data point, add more fully connected: ACC 86.75%

Notebook: Enhance_Deep_Feature_2.ipynb

Best weight: https://drive.google.com/file/d/1FBPpl-LjLeV72JQznXVeHCbQV7EqOzjD/view?usp=sharing

# Ablation

Goal: Apply other approaches but keep the same number of parameters (or pitiful)

## CNN (as feature extractor - Mobilenet 0.25) + LSTM

Worst, only ACC 60% on val set => no need to store weight

Notebook: CNN_LSTM

## ConvLSTM2D

Notebook: ConvLSTM2D

ACC: 74 val set

Best weight: https://drive.google.com/file/d/1vlA83dcw-gh59SyuqD6_UpmDL0K-FcW_/view?usp=sharing

## Demo
Notebook :Demo

goal:output a violence detection result on your video


modify the video_input change the following text into your video path

video_input = '/content/drive/MyDrive/video/video1.mp4'


modify the video_input change the following text into your target path

video_output = '/content/drive/MyDrive/video/output1.mp4'


run all cell and you will get the result video in your target path

## Validation
Notebook: Validation

goal:check model accuary by using validation data

unzip the validation data

unzip val.zip

modify the val_path change the following text into your val data path

val_path = '/content/val'

run all cell and you will see the val accuary
