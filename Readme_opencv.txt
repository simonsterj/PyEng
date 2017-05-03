DIRECTIONS: Install OpenCV3 with Python3 with FFMPEG

Method 1: Unsuccessful
Method 2: Unsuccessful


METHOD 1:
UNSUCCESSFUL
Error: ImportError: No module named ‘cv2’


INSTALLATION STEPS TAKEN/COMMANDS GIVEN:

Create VM running 64 bit Ubuntu 16.04
Python version: 3.5.2


INSTALL PACKAGES
>>> sudo apt-get update
>>> sudo apt-get install build-essential cmake git libgtk2.0-dev pkg-config ffmpeg
>>> sudo apt-get install python3.5-dev


COPY PYTHON DEV FILE
>>> sudo cp /usr/include/x86_64-linux-gnu/python3.5m/pyconfig.h /usr/include/python3.5m/


DL OPENCV SOURCE
>>> mkdir OpenCV-tmp
>>> cd OpenCV-tmp
>>> git clone https://github.com/Itseez/opencv.git
>>> mv opencv opencv-3


BUILDING
>>> mkdir build
>>> cd build
>>> cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local ../opencv-3

>>> make -j $(nproc --all)


INSTALL
>>> sudo make install


CHECKING
>>> python3
>>> import cv2
ImportError: No module named ‘cv2’






METHOD 2:
UNSUCCESSFUL
NOTE: Does not come compiled with FFMPEG

INSTALLATION STEPS TAKEN/COMMANDS GIVEN:

Create VM running 64 bit Ubuntu 16.04
Python version: 3.5.2
Using OpenCV on Wheels
https://pypi.python.org/pypi/opencv-python


INSTALL PACKAGES
>>> pip3 install opencv-python


CHECK INSTALLATION
python3
Python 3.5.2 (default, Nov 17 2016, 17:05:23) 
[GCC 5.4.0 20160609] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import cv2
>>> cv2.__version__
'3.2.0'
