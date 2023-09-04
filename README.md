# Test Datasets for Individual Pig Tracking 
This repository contains the test datasets used in the paper.

A. Jaoukaew, W. Suwansantisuk, P. Kumhom, “Robust individual pig tracking,” International Journal of Electrical and Computer Engineering, Accepted for publication.
## Please cite the above paper if you use the datasets in this repository.
The GT_and_VDOs_Pigs folder contains four datasets (Videos 1-4), which serve to evaluate the methods of pig’s  identification and tracking. It also contains the corresponding ground truth files, which specify actual bounding boxes over the head and body of each pig.

Each test video contained 5,000 continuous frames, taken from a top-view camera over a pen. There are ten pigs in each video frame. Videos 1-3 were captured in the morning, midday, and evening, respectively. The pig, pen, and camera setup in videos 1-3 were the same as those in the videos used in training the Faster region-based convolutional neural network (Faster R-CNN) model in the paper. Video 4 had a different camera setup, pen, and pigs from the video used in training the Faster R-CNN model. Videos 1-3 were taken from an environment familiar to the pig detection model, while video 4 was not. Videos 1-4 tested the abilities of the detection and tracking methods under various conditions.

Each ground truth file contains the bounding boxes over the pigs’ heads and bodies for ten frames, down sampled from 5,000 continuous frames of the corresponding test video. Ground truth files were presented in the CSV file format. The files are GT_VDO1.csv, GT_VDO2.csv, GT_VDO3.csv, and GT_VDO4.csv, which are for the test videos 1-4, respectively. Columns of each CSV and their descriptions are as follows:

•	_**VDO_frame**_ : The frame number in the corresponding test video.

•	_**pigID**_ : A unique identification of each pig. In a given CSV file, pigs that appear in different VDO frames but have the same pigID are the same pig.

•	_**(head_xmin, head_ymin)**_ : The point on the upper-left corner of the bounding box over the  head of the pig, whose unique identification is pigID.

•	_**(head_xmax, head_ymax)**_ : The point on the lower-right corner of the bounding box over the  head of the pig, whose unique identification is pigID.

•	_**(body_xmin, body_ymin)**_ : The point on the upper-left corner of the bounding box over the  body of the pig, whose unique identification is pigID.

•	_**(body_xmax, body_ymax)**_ : The point on the lower-right corner of the bounding box over the  body of the pig, whose unique identification is pigID.

Each ground truth file provides the actual locations of the bounding boxes over the head and body of each pig.
