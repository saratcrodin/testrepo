26-7-2022				
No	Item	Description/Comments	Status	Misc Info
1	Get ORB SLAM 3 to work	Get ORB SLAM 3 source. Compile and install. Run few examples.	Done	Have done this on a laptop and also a VM. Made a reference doc with installation steps for future references.
2	Baseline Step1: ORB SLAM3 with Laptop webcam	ORB SLAM 3 must run with the Webcam in the laptop	In Progress	" -tried to run on Ubuntu 22. Had compatibility issues with python versions. Impact on ORB SLAM3 dependencies due to multiple co-existing python versions
-Tried running on a VM(Ubuntu 20). Basic run successful. But crahes and tracking freezes inconsistently.
tried to run on Ubuntu 20. Having issues with ROS node compilation. 
-Melodic not supported on 20. Neotic is supported. But ORB SLAM3 depends on pythininterp 2.7 but neotic needs > 3
Next step is to downgrade to Ubuntu 18"
3	ORB SLAM 3 implementation overall underatanding	Understand the code, modules, etc.	In Progress	" -No documentation explaining internals
-tried to reverse engineer the executable, proved too difficult.dropped
-tried to generate doxygen control flow graphs, but insufficient
-must try updating comments and then generating graphs"
4	AKAZE vs ORB	Make a strong case for motivation as to why AKAZE was chosen	Pending	
