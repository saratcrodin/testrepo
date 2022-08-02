Week 1: 26-7-2022
|No	|Item	|Description/Comments	|Status	|MiscInfo |
|---|-----|---------------------|-------|---------|
1	|Get ORB SLAM 3 to work	|Get ORB SLAM 3 source. Compile and install. Run few examples.	|Done	|Have done this on a laptop and also a VM. Made a reference doc with installation steps for future references.|
2 |Baseline Step1: ORB SLAM3 with Laptop webcam |ORB SLAM 3 must run with the Webcam in the laptop |In Progress | -tried to run on Ubuntu 22. Had compatibility issues with python versions. Impact on ORB SLAM3 dependencies due to multiple co-existing python versions <br/>-Tried running on a VM(Ubuntu 20). Basic run successful. But crahes and tracking freezes inconsistently. <br/>-tried to run on Ubuntu 20. Having issues with ROS node compilation.<br/>-Melodic not supported on 20. Neotic is supported. But ORB SLAM3 depends on pythininterp 2.7 but neotic needs > 3  Next step is to downgrade to Ubuntu 18|
3 |ORB SLAM 3 implementation overall underatanding |Understand the code, modules, etc. |In Progress | -No documentation explaining internals <br/>-tried to reverse engineer the executable, proved too difficult.dropped <br/>-tried to generate doxygen control flow graphs, but insufficient <br/>-must try updating comments and then generating graphs
4 |AKAZE vs ORB |Make a strong case for motivation as to why AKAZE was chosen |Pending | |


| Method | Value |
| :---: | :---: |
| cv2.TM_CCOEFF_NORMED | 0.282997101545 |
| cv2.TM_CCORR_NORMED | 0.79689925909 |
| cv2.TM_SQDIFF_NORMED | 0.447067975998 |
