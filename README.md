# Marilia_Furman-PSM_Gallery
**Technical setup for Marilia Furman's artwork**

### Description

An object recognition system which triggers subtitles on the top of the video stream of a webcam, according to the objects being recognized in real time. Implemented by Fernando Visockis in vvvv for the artist's exhibition in PSM Gallery Berlin, June 2019.



### Overview

The system runs in vvvv (beta 38.1). For object recognition functionalities it uses Yolo V2, VL.OpenCV.  The camera used to run it is a Logitech HD Webcam C615

### Dependencies

Vl.OpenCV

DX11 pack

VL.Skia

A custom made Json parser library (present in this repo, but could be replaced by other similar solutions)



### Instructions

Open the args.txt in the vvvv directory and put there "/package-repositories "[LINK]"". Where the [LINK] is the path to the inside of "**Marilia_Furman-PSM_Gallery** ". This is needed, because the Yolo integration is based on customized VL.OpenCV which is included in the Repo. It can be changed when the Yolo will be officially integrated into the VL.OpenCV pack hosted at the Nuget server.

The Yolo models (.weight) had to be removed from this repo due to its size. They can be found in here: https://pjreddie.com/media/files/yolov2.weights

For use with the COCO Dataset (80 classes):

1) Download Cfg file:
https://raw.githubusercontent.com/pjreddie/darknet/master/cfg/yolov2.cfg

2) Download Darknet Model:
https://pjreddie.com/media/files/yolov2.weights

3) Download Labels:
https://raw.githubusercontent.com/pjreddie/darknet/master/data/coco.names

References:
Yolo V2: https://pjreddie.com/darknet/yolov2/
COCO Dataset: http://cocodataset.org/#explore

