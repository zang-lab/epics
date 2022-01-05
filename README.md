# EPICS
Extracting Physical-Characteristics from Images of Chromatin Structures (EPICS) is a machine-learning based computational method for processing high-resolution chromatin 3D image data. 

## Repository Organization

Each of the experiments associated with EPICS is provided in respective branches.  Specifically, experiments were done on 3D-EMISH and 3D-SIM data.  Those experiments (code, associated data, and output) are all provided in their respective branches.  The .py files in each branch collect the features from the raw data.  The .r files build the models for classifying open and closed chromatin domains (CDs).   

## Data

Raw 3D-EMISH data was obtained from Trzaskoma et.al.'s GitHub (https://github.com/3DEMISH/3D-EMISH).  Raw 3D-SIM images were obtained from Cremer et.al.'s 2020 paper.   

## System Information

The computation was performed on a Ubuntu 18.04.5 system with 64 GB of RAM and an Intel® Xeon(R) W-2245 CPU @ 3.90GHz with 8 cores and 16 threads.  Below is a list of the installed versions of the Python libraries (as of Janurary 2021):


