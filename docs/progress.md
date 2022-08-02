
Week 1: 26-7-2022
--

|No			|Item			|Description/Comments			|Status			|Misc Info|		
| :--- |			:--- |			:--- |			:--- |			:--- |		
|<font size=2>	1	</font>|	<font size=2>	Get ORB SLAM 3 to work	</font>|	<font size=2>	Get ORB SLAM 3 source. Compile and install. Run few examples.	</font>|	<font size=2>	Done	</font>|	<font size=2>	Have done this on a laptop and also a VM. Made a reference doc with installation steps for future references.	</font>|
|<font size=2>	2	</font>|	<font size=2>	Baseline Step1: ORB SLAM3 with Laptop webcam	</font>|	<font size=2>	ORB SLAM 3 must run with the Webcam in the laptop	</font>|	<font size=2>	In Progress	</font>|	<font size=2>	 -tried to run on Ubuntu 22. Had compatibility issues with python versions. Impact on ORB SLAM3 dependencies due to multiple co-existing python versions<br/>-Tried running on a VM(Ubuntu 20). Basic run successful. But crahes and tracking freezes inconsistently.<br/>-tried to run on Ubuntu 20. Having issues with ROS node compilation. <br/>-Melodic not supported on 20. Neotic is supported. But ORB SLAM3<br/>-depends on pythininterp 2.7 but neotic needs > 3<br/>Next step is to downgrade to Ubuntu 18	</font>|
|<font size=2>	3	</font>|	<font size=2>	ORB SLAM 3 implementation overall underatanding	</font>|	<font size=2>	Understand the code, modules, etc.	</font>|	<font size=2>	In Progress	</font>|	<font size=2>	 -No documentation explaining internals<br/>-tried to reverse engineer the executable, proved too difficult.dropped<br/>-tried to generate doxygen control flow graphs, but insufficient<br/>-must try updating comments and then generating graphs	</font>|
|<font size=2>	4	</font>|	<font size=2>	AKAZE vs ORB	</font>|	<font size=2>	Make a strong case for motivation as to why AKAZE was chosen	</font>|	<font size=2>	Pending	</font>|	<font size=2>		</font>|

Week 2: 2-8-2022
--

|No			|Item			|Description/Comments			|Status			|Misc Info|		
| :--- |			:--- |			:--- |			:--- |			:--- |		
|<font size=2>	1	</font>|	<font size=2>	AKAZE vs ORB	</font>|	<font size=2>	Make a strong case for motivation as to why AKAZE was chosen	</font>|	<font size=2>	Done	</font>|	<font size=2>	ORB is faster, but AKAZE is better - AKAZE has Better matching and is Scale invariant. ORB is not scale invariant. AKAZE performs well with low resolution images (640x480). Performance drops with higher resolution. Probably due to non linear scale space.<br/>if we have AKAZE working in real time , then even if there is ORB in HW acceleration, if real time speed is achieved, then AKAZE would be the winner. Bcos if I have real time performance doesn’t matter if it is few nanoseconds slower. But need proof for this.<br/>Can we compare HW based AKAZE with SW based ORB.<br/>is there Hardware based ORB that can be used for comparison<br/>AKAZE is always only preferred for low resolution and not for high resolution<br/>Bottlenose is HD camera, how do we justify this ?<br/>there is HW accelerated ORB. <br/>[paper1](https://ieeexplore.ieee.org/document/9651662) <br/> [paper2](https://upcommons.upc.edu/bitstream/handle/2117/176803/144679.pdf?sequence=1&isAllowed=y#:~:text=by%20Ra%C3%BAl%20TARANCO,an%20agent's%20location%20within%20it.) <br/> ORB has also improved by adding scale invariance.<br/>[paper1](https://dl.acm.org/doi/abs/10.1145/3297156.3297184)</font>|
|<font size=2>	2	</font>|	<font size=2>	ORB SLAM 3 implementation overall underatanding	</font>|	<font size=2>	Understand the code, modules, etc.	</font>|	<font size=2>	In Progress	</font>|	<font size=2>	pin tool usage was challenging<br/> did not attempt clang llvm compilation<br/> valgrind + Kcachegrind worked to some extent.<br/>Doxygen worked to some extent<br/> Will use these two and proceed<br/> 	</font>|


