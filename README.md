# TrackingBee

TrackingBee is a simple real-time multi-object tracker (MOT) that works for any kind of object class (not just people).
 
## Introduction

TrackingBee is designed to be a state-of-the-art (SOTA) multi-object tracker (MOT) for use on your own projects. And bcause the You-only-look-once algorithm (YOLO) detector is pretrained on COCO dataset. Simple Online Realtime Tracking algorithm (SORT) is using tracking all bee members at the hive door
Modifying it is exactly the same process as training YOLO with your own dataset.(https://github.com/ultralytics/yolov5/wiki/Train-Custom-Data)

**TrackingBee by SORT implements** 
+ [ultralytics/YOLOv5](https://github.com/ultralytics/yolov5/wiki) with no modifications
+ [abewley/SORT](https://github.com/abewley/sort) with minor modifications 

This repository uses a fixed version of YOLOv5 to ensure compatbility. Replacing the YOLOv5 code to the updated ultralytics/YOLOv5 code may result in breaking changes. In this repo use YOLOv5 v4 
https://github.com/ultralytics/yolov5/releases/tag/v4.0
## Using TrackingBee

Clone this repository

```bash
git clone https://github.com/HieuVV1804/Tracking_Bee.git
cd Tracking_Bee
```

### Install Requirements

Python 3.8 or later with all requirements.txt. To install run:

```bash
pip install -r requirements.txt
```

### Download YOLOv5 weights

```bash
./download_weights.sh
```
This script will save yolov5 weights to `yolov5/weights/` directory.

### Run Tracking

To run the tracker on your own video and view the tracked bounding boxes, run:

```bash
python classy_track1.py --source /path/to/video.mp4 --view-img
```

To get a summary of arguments run:

The text results are saved to `/inference/output/` from the array above in the following format.

The saved text file contains the following information:

```bash
[frame_index, x_center, y_center, object_id, count]
```

where

+ x_center: x center coordinates of bbox
+ y_center: y center coordinates of bbox
+ count: total number of bees in 1 frame


![image](https://user-images.githubusercontent.com/106183467/186697442-01200d8e-e81d-4b70-bfc9-bb7f70caf253.png)

