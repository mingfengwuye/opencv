# opencv
build opencv


Install requirement
[compiler] sudo apt-get install build-essential

[required] sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev

[optional] sudo apt-get install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev

[Pull code]
cd ~/<my_working_directory>
git clone https://github.com/opencv/opencv.git
git clone https://github.com/opencv/opencv_contrib.git

BUILD

cd ~/opencv
mkdir build
cd build

[support dnn]
cmake -D CMAKE_BUILD_TYPE=Release 
-DOPENCV_EXTRA_MODULES_PATH=<opencv_contrib>/modules 
-D BUILD_opencv_dnn=ON
-D CMAKE_INSTALL_PREFIX=/usr/local ..


Make
Make install


Running tests
git clone https://github.com/opencv/opencv_extra.git

set OPENCV_TEST_DATA_PATH environment variable to <path to opencv_extra/testdata>
<cmake_build_dir>/bin/opencv_test_core

