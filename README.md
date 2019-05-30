## **s5pxx18-opencv-uvccamera-cpp-demo**

Build
------------
```
git clone https://github.com/friendlyarm/s5pxx18-opencv-uvccamera-cpp-demo.git
cd s5pxx18-opencv-uvccamera-cpp-demo
mkdir build
cd build
cmake ..
make
```

Run one camera
------------
```
. /usr/bin/setqt5env-eglfs
./opencamera 1
```

Run two cameras
------------
```
. /usr/bin/setqt5env-eglfs
./opencamera 2
```

Reading mjpeg stream
------------
open the camera using the following code:
```
pCapture[i] = new VideoCapture(get_camerasrc_mjpeg(devIndex),cv::CAP_GSTREAMER);
```

Reading NV12 stream
------------
open the camera using the following code:
```
pCapture[i] = new VideoCapture(get_camerasrc_nv12(devIndex),cv::CAP_GSTREAMER);
```

Supported camera
------------
```
Logitech C922 (NV21, MJPG)
KS2A242  (NV21, MJPG)
```

Supported boards
------------
* S5P6818   
NanoPC T3/T3 Plus  
NanoPi Fire3  
Smart6818  
NanoPi M3
* S5P4418  
NanoPC T2 Plus  
NanoPi Fire2a  
Smart4418  
NanoPi S2  
NanoPi M2/M2a  

How can i find out the supported camera resolutions
------------
```
v4l2-ctl --list-formats-ext -d /dev/video0
```

More examples
------------
https://github.com/friendlyarm/rk3399-opencv-uvccamera-cpp-demo  
https://github.com/friendlyarm/rk3399-opencv-ucvcamera-python-demo  
https://github.com/friendlyarm/install-opencv-on-friendlycore  

