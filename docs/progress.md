Week 1: 26-7-2022
---
|No			|Item			|Description/Comments			|Status			|Misc Info|		
| :--- |			:--- |			:--- |			:--- |			:--- |		
|<font size=2>	1	</font>|	<font size=2>	Get ORB SLAM 3 to work	</font>|	<font size=2>	Get ORB SLAM 3 source. Compile and install. Run few examples.	</font>|	<font size=2>	Done	</font>|	<font size=2>	Have done this on a laptop and also a VM. Made a reference doc with installation steps for future references.	</font>|
|<font size=2>	2	</font>|	<font size=2>	Baseline Step1: ORB SLAM3 with Laptop webcam	</font>|	<font size=2>	ORB SLAM 3 must run with the Webcam in the laptop	</font>|	<font size=2>	In Progress	</font>|	<font size=2>	 -tried to run on Ubuntu 22. Had compatibility issues with python versions. Impact on ORB SLAM3 dependencies due to multiple co-existing python versions<br/>-Tried running on a VM(Ubuntu 20). Basic run successful. But crahes and tracking freezes inconsistently.<br/>-tried to run on Ubuntu 20. Having issues with ROS node compilation. <br/>-Melodic not supported on 20. Neotic is supported. But ORB SLAM3<br/>-depends on pythininterp 2.7 but neotic needs > 3<br/>Next step is to downgrade to Ubuntu 18	</font>|
|<font size=2>	3	</font>|	<font size=2>	ORB SLAM 3 implementation overall underatanding	</font>|	<font size=2>	Understand the code, modules, etc.	</font>|	<font size=2>	In Progress	</font>|	<font size=2>	 -No documentation explaining internals<br/>-tried to reverse engineer the executable, proved too difficult.dropped<br/>-tried to generate doxygen control flow graphs, but insufficient<br/>-must try updating comments and then generating graphs	</font>|
|<font size=2>	4	</font>|	<font size=2>	AKAZE vs ORB	</font>|	<font size=2>	Make a strong case for motivation as to why AKAZE was chosen	</font>|	<font size=2>	Pending	</font>|	<font size=2>		</font>|

Week 2: 2-8-2022
---
|No			|Item			|Description/Comments			|Status			|Misc Info|		
| :--- |			:--- |			:--- |			:--- |			:--- |		
|<font size=2>	1	</font>|	<font size=2>	Baseline Step1: ORB SLAM3 with Laptop webcam	</font>|	<font size=2>	ORB SLAM 3 must run with the Webcam in the laptop	</font>|	<font size=2>	Done	</font>|	<font size=2>	[orbslam3_webcam_run1.mkv](https://cmailcarletonca-my.sharepoint.com/:v:/r/personal/mohamedatia_cunet_carleton_ca/Documents/Sarat MAS Progress/orbslam3_webcam_run1.mkv?csf=1&web=1&e=S8wRyZ)	</font>|
|<font size=2>	2	</font>|	<font size=2>	AKAZE vs ORB	</font>|	<font size=2>	Make a strong case for motivation as to why AKAZE was chosen	</font>|	<font size=2>	Done	</font>|	<font size=2>	ORB is faster, but AKAZE is better - AKAZE has Better matching and is Scale invariant. ORB is not scale invariant. AKAZE performs well with low resolution images (640x480). Performance drops with higher resolution. Probably due to non linear scale space.<br/>if we have AKAZE working in real time , then even if there is ORB in HW acceleration, if real time speed is achieved, then AKAZE would be the winner. Bcos if I have real time performance doesn’t matter if it is few nanoseconds slower. But need proof for this.<br/>Can we compare HW based AKAZE with SW based ORB.<br/>is there Hardware based ORB that can be used for comparison<br/>AKAZE is always only preferred for low resolution and not for high resolution<br/>Bottlenose is HD camera, how do we justify this ?<br/>there is HW accelerated ORB. <br/>[paper1](https://ieeexplore.ieee.org/document/9651662) <br/> [paper2](https://upcommons.upc.edu/bitstream/handle/2117/176803/144679.pdf?sequence=1&isAllowed=y#:~:text=by%20Ra%C3%BAl%20TARANCO,an%20agent's%20location%20within%20it.) <br/> ORB has also improved by adding scale invariance.<br/>[paper1](https://dl.acm.org/doi/abs/10.1145/3297156.3297184)	</font>|
|<font size=2>	3	</font>|	<font size=2>	ORB SLAM 3 implementation overall underatanding	</font>|	<font size=2>	Understand the code, modules, etc.	</font>|	<font size=2>	In Progress	</font>|	<font size=2>	pin tool usage was challenging<br/> did not attempt clang llvm compilation<br/> valgrind + Kcachegrind worked to some extent.<br/>Doxygen worked to some extent<br/> Will use these two and proceed<br/> 	</font>|

Week 3: 08-09-2022														
---

Week 4: 16-8-2022														
---

Week 5: 23-8-2022														
---

Week 6: 30-8-2022														
---
|No			|Item			|Description/Comments			|Status			|Misc Info|		
| :--- |			:--- |			:--- |			:--- |			:--- |		
|<font size=2>	1	</font>|	<font size=2>	ORB SLAM 3 implementation overall underatanding	</font>|	<font size=2>	Understand the code, modules, etc.	</font>|	<font size=2>	In Progress	</font>|	<font size=2>	Going on in parallel as the examples are studied	</font>|
|<font size=2>	2	</font>|	<font size=2>	Understading the Go Pro solution	</font>|	<font size=2>	compare ORB SLAM 3 with Go Pro 3 solution code base and identify the differences	</font>|	<font size=2>	In Progress	</font>|	<font size=2>	Calibration for different go pro settings - all the new yaml files in the example folder<br/>new camera model- double sphere<br/>significance of this camera model is not clear.<br/>	</font>|
|<font size=2>	3	</font>|	<font size=2>	Solution for Rolling shutter	</font>|	<font size=2>	Understand all basics. Analyse existing solutions for rolling shutter in research	</font>|	<font size=2>	In Progress	</font>|	<font size=2>	Identified papers. Study in progress<br/>Imu data can be used<br/>machine learning can be used<br/>	</font>|
|<font size=2>	4	</font>|	<font size=2>	Run ORB SLAM3 with all other datasets	</font>|	<font size=2>	Run ORB SLAM3 with TUM, EUROC, KITTI	</font>|	<font size=2>	Done	</font>|	<font size=2>	able to run tum, euric, kitti. Issues in the code are fixed. <br/>Trying to understand if we can prefer any datasets/sequences.<br/>	</font>|
|<font size=2>	5	</font>|	<font size=2>	ORB SLAM 3 with Bottlenose dataset	</font>|	<font size=2>	Run ORB SLAM 3 with Bottlenose dataset	</font>|	<font size=2>	In Progress	</font>|	<font size=2>	Minor updates needed in the dataset provided.<br/>if system can take frames as input, giving key frames as input must be possible, we might need to skip the extraction part and feed the keyframe data that we already have. Not sure if this is needed. Just having it in task backlog<br/>what is the frame rate, shutter speed (https://shotkit.com/what-is-shutter-speed/)?	</font>|
|<font size=2>	6	</font>|	<font size=2>	Metrics	</font>|	<font size=2>	identify what metrics we need to observe in order to compare the improvements or existing dataset based runs	</font>|	<font size=2>	In Progress	</font>|	<font size=2>	ATE and timing. Timing can be captured from any point. Trajectory is saved as text file, but how to realise it in map and how to compare is not clear. <br/>Lack of IMU for us, this will impact ATE. Need to make sure fair comparison done.	</font>|
|<font size=2>	7	</font>|	<font size=2>	Impact of image resolution	</font>|	<font size=2>	how does resolution impact SLAM. Is 8MP cam > 2MP cam for SLAM. Ignore Cpu requirements.	</font>|	<font size=2>	Done	</font>|	<font size=2>	high resolution impacts real time performance<br/>(https://github.com/raulmur/ORB_SLAM2/issues/35)<br/>also observe that they resize images in examples optimum resolution, optimum number of features is better choice for real time performance	</font>|

Week 7: 30-8-2022														
---
|No			|Item			|Description/Comments			|Status			|Misc Info|		
| :--- |			:--- |			:--- |			:--- |			:--- |		
|<font size=2>	1	</font>|	<font size=2>	Understanding Calibration	</font>|	<font size=2>	Understand Calibration process for ORB SLAM3<br/>Calibrate webcam, zed, realsense	</font>|	<font size=2>		</font>|	<font size=2>		</font>|
|<font size=2>	2	</font>|	<font size=2>	Run calibration and run ORB SLAM 3	</font>|	<font size=2>	Calibrate the webcam and run ORB SLAM3. Identify if there is any improvement	</font>|	<font size=2>		</font>|	<font size=2>		</font>|
|<font size=2>	3	</font>|	<font size=2>	Baseline Step2: ORB SLAM3 with Realsense	</font>|	<font size=2>	ORB SLAM 3 must run with the realsense camera<br/>Also try Zed	</font>|	<font size=2>		</font>|	<font size=2>		</font>|
