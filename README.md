# _Multi-Camera Person Tracking and Re-Identification_ (using video)

## Introduction
This project aims to track people in different videos accounting for different angles. 


The framework used to accomplish this task relies on MOT and ReID to track and re-identify ID's of humans, respectively.  
The tracking can be completed using YOLO_v3 or YOLO_v4 and ReID relies on KaiyangZhou's Torchreid library.
  
## Installation  
 - Download [Anaconda](https://www.anaconda.com/products/individual) if it is not installed on your machine

 - Clone the repository
```python
git clone https://github.com/samihormi/Multi-Camera-Person-Tracking-and-Re-Identification
```
- Create a project environment
```python
cd Multi-Camera-Person-Tracking-and-Re-Identification
conda create --name py37 python=3.7
conda activate py37
```
- Install dependencies
```python
pip install -r requirements.txt
```
- Install torch and torchvision based on the cuda version of your machine
```python
conda install pytorch torchvision cudatoolkit -c pytorch
```
## Convert models
- Download the YOLO models for [YOLO_v3](https://drive.google.com/file/d/18fmQMegNsAzPte7tJeCxwf1iE8JUTQhQ/view?usp=sharing) and [YOLO_v4](https://drive.google.com/file/d/1w9furPagm3KytRW2uNooLcBoiYWDwbop/view?usp=sharing) and add them to /model_data/weights/

* YOLO_v4
```python
python convert_y4.py model_data\weights\yolov4.weights model_data\models\yolov4.h5
```
## Demo 
```python
python demo.py --videos videos\init\Double1.mp4 videos\init\Single1.mp4 --version v3
```
