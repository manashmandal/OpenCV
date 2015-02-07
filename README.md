# OpenCV
All about opencv in qt


## Sample of Pro file
```
QT       += core

QT       -= gui

TARGET = untitled
CONFIG   += console
CONFIG   -= app_bundle

TEMPLATE = app


SOURCES += main.cpp
INCLUDEPATH += C://opencv//sources//release//install//include

CONFIG -= qt

LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_calib3d2410.dll.a

LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_contrib2410.dll.a

LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_core2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_features2d2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_flann2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_gpu2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_highgui2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_imgproc2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_legacy2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_ml2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_nonfree2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_objdetect2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_ocl2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_photo2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_stitching2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_superres2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_ts2410.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_video2410.dll.a
LIBS += C://opencv//sources//release//install//x64//mingw//lib//libopencv_videostab2410.dll.a

```


## Sample of a program

```cpp
#include "opencv2/opencv.hpp"
#include "opencv2/highgui/highgui.hpp"

using namespace cv;

int main(int argc, char** argv)
{
    namedWindow("Output", 1);
    Mat output = Mat::zeros(120, 350, CV_8UC3);
    putText(output, "Hello world", cvPoint(15,70), FONT_HERSHEY_PLAIN, 3 , cvScalar(0,255,0),4);
    imshow("Output", output);
    waitKey(0);
    return 0;
}
```
