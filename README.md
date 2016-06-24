# DENG_TCSVT
Subjective-driven Complexity Control Source Code

The software code is for the paper "Subjective-driven Complexity Control Approach for HEVC". Before you run the code, you need to set some values in the code according to your needs.

1. TEncTop.cpp 
In line 1183 and 1184, you need to set the width and height of the test video. The resolutions suppoerted in this code include 1920x1080, 1280x720, and 832x480. 
In line 1185, you need to set the target complexity, which can be chosen from {80, 60, 40 20}.

2. TEncSlice.cpp
In line 681, you need to modify the .txt file name according to the test video. This file is the subjective weight map of the test video, which can be found in ".\Deng_TCSVT_Code\bin\vc10\Win32\Debug". Here, the subjective weight map we provided only includes the first 300 frames, thus you should set the number of encoded frame to be 300 in configuration file. If you want to run more frames, you can generate the subjective weight maps by yourself according to the paper "A novel multiresolution spatiotemporal saliency detection model and its applications in image  and video compression,” Image Processing, IEEE Transactions on, vol. 19, no. 1, pp. 185–198, 2010.

After runing the code, you can find a out.txt file in .\Deng_TCSVT_Code\bin\vc10\Win32\Debug, which records the running time and PSNR value of each frame. 
