
Week 1: 26-7-2022


| No	| Item	| Description/Comments	| Status	| MiscInfo |
| :--- | :----- | :--------------------- | :------- | :--------- |
| 1	| <font size=1> Get ORB SLAM 3 to work	</font> | <font size=2> Get ORB SLAM 3 source. Compile and install. Run few examples.	</font> | <font size=3> Done	</font> | <font size=4> Have done this on a laptop and also a VM. Made a reference doc with installation steps for future references. </font> |
| 2 | Baseline Step1: ORB SLAM3 with Laptop webcam | ORB SLAM 3 must run with the Webcam in the laptop | In Progress | -tried to run on Ubuntu 22. Had compatibility issues with python versions. Impact on ORB SLAM3 dependencies due to multiple co-existing python versions <br/>-Tried running on a VM(Ubuntu 20). Basic run successful. But crahes and tracking freezes inconsistently. <br/>-tried to run on Ubuntu 20. Having issues with ROS node compilation.<br/>-Melodic not supported on 20. Neotic is supported. But ORB SLAM3 depends on pythininterp 2.7 but neotic needs > 3  Next step is to downgrade to Ubuntu 18 |
| 3 | ORB SLAM 3 implementation overall underatanding | Understand the code, modules, etc. | In Progress | -No documentation explaining internals <br/>-tried to reverse engineer the executable, proved too difficult.dropped <br/>-tried to generate doxygen control flow graphs, but insufficient <br/>-must try updating comments and then generating graphs |
| 4 | AKAZE vs ORB | Make a strong case for motivation as to why AKAZE was chosen |Pending | |
  
Week 2: 2-8-2022

| No	| Item	| Description/Comments	| Status	| MiscInfo |
| :--- | :----- | :--------------------- | :------- | :--------- |
| 1	| AKAZE vs ORB | Make a strong case for motivation as to why AKAZE was chosen | Done | |
| 2 | ORB SLAM 3 implementation overall underatanding | Understand the code, modules, etc. | In Progress | |


|No			|Item			|Description/Comments			|Status			|Misc Info|		
| :--- |			:--- |			:--- |			:--- |			:--- |		
|<font size=2>	1	</font>|	<font size=2>	Get ORB SLAM 3 to work	</font>|	<font size=2>	Get ORB SLAM 3 source. Compile and install. Run few examples.	</font>|	<font size=2>	Done	</font>|	<font size=2>	Have done this on a laptop and also a VM. Made a reference doc with installation steps for future references.	</font>|
|<font size=2>	2	</font>|	<font size=2>	Baseline Step1: ORB SLAM3 with Laptop webcam	</font>|	<font size=2>	ORB SLAM 3 must run with the Webcam in the laptop	</font>|	<font size=2>	In Progress	</font>|	<font size=2>	 -tried to run on Ubuntu 22. Had compatibility issues with python versions. Impact on ORB SLAM3 dependencies due to multiple co-existing python versions<br/>-Tried running on a VM(Ubuntu 20). Basic run successful. But crahes and tracking freezes inconsistently.<br/>-tried to run on Ubuntu 20. Having issues with ROS node compilation. <br/>-Melodic not supported on 20. Neotic is supported. But ORB SLAM3<br/>-depends on pythininterp 2.7 but neotic needs > 3<br/>Next step is to downgrade to Ubuntu 18	</font>|
|<font size=2>	3	</font>|	<font size=2>	ORB SLAM 3 implementation overall underatanding	</font>|	<font size=2>	Understand the code, modules, etc.	</font>|	<font size=2>	In Progress	</font>|	<font size=2>	 -No documentation explaining internals<br/>-tried to reverse engineer the executable, proved too difficult.dropped<br/>-tried to generate doxygen control flow graphs, but insufficient<br/>-must try updating comments and then generating graphs	</font>|
|<font size=2>	4	</font>|	<font size=2>	AKAZE vs ORB	</font>|	<font size=2>	Make a strong case for motivation as to why AKAZE was chosen	</font>|	<font size=2>	Pending	</font>|	<font size=2>		</font>|





