# AquaBoxDataset 
A dataset for bounding box prediction in underwater environments of the Aqua-family of hexapod robots. This dataset has hand-made annotations 

The dataset is made available under the releases section as two .zip files: VALID.zip and TRAINING.zip. 

The TRAINING.zip file contains data from 2015 and 2016 collected near the reef outside McGill Bellairs Research Institute in Barbados.

Directory structure of the releases:

<pre>
VALID/TRAINING
    --> <folder_name> (capture session)
        --> img (raw images)
            --> NNNN.jpg
        --> yolo_out (pre-computed yolo features/outputs) 
            --> NNNN.npy
        groundtruth_rect.txt (ground truth bounding box values)
        annotations.pkl (original raw annotations file)
</pre>
        
Descriptions:

<pre>
yolo_out:

pre-computed yolo features of size 1080 with the last 6 values being
[class_confidence, x_center, y_center, width, height, confidence]
of the highest confidence yolo bounding box prediction all normalized
by the image width and height respectively

groundtruth_rect.txt:

ground truth hand-made annotations of format
[x_center, y_center, width, height] of the bounding box,
all normalized by the image width and height respectively
</pre>

        
If you use this dataset, please cite:

TODO
