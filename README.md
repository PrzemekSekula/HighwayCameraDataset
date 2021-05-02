# HighwayCameraDataset
Code for organizing and preprocessing an object detection related dataset.

This repository is prepared to deal with an object detection related dataset build with a matlab labelling tool. This repository is a part of one of CATT projects, to use it fully you need to have access to all the relevant resources. Right now we are not sharing the dataset yet.

# What's inside
- ./data/ - this folder contains .xlsx files with labels (bounding boxes)
- ./tfrecord/ Folder for .tfrecord files.
- ./data/data.csv - allows to connect the labels with the videos. The columns in this file are as follows 
    - label - name of .xlsx file with labels
    - video - name (with full path) to the related video (**TODO**: make the paths relative)
    - shift - sometimes the frames from the `label` files do not fit to the frames from the `video` file (I do not know why) and it is necessary to shift it. If so, this column informs us about the size and direction of shift (it is in the number of frames)
     
- Analysis - used for initial data analysis
- Create_tfrecord - used for generating .tfrecord files
- ViewData - used for previewing data frame by frame
- ViewDataDemo - (obsolete) - like ViewData, but it uses file paths instead of ./data/data.csv files

# Credits
The dataset is labeled by:
- QingLian He (team leader)
- Binya Zhang
- Amir Noekhan

# TODO
- Continue building dataset. It is still under construction.
- Add debuging to `Create_tfrecord.ipynb`. I wnat no know if the frames in .tfrecord files are being generated correctly
- Aggregate the common functions in a library. Dealing with data.csv and the entire content of ./data should be unified across all the notebooks.
- Clean and refactor the code, make all the pathes relative, add function descriptions etc.
- Add a brief description of the labelling process. It should include at least the name of the app, the outcomes and the postprocessing (from matlab file to .xlsx)
- Add QingLian's Matlab code that changes matlab files into .xlsx or write something similar in python, to have the entire pipeline in one place


