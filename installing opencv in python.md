# Installing openCV 3 in both python and Qt
* Before proceeding download the following files
  * `Python27 32-bit`
  * `NumPy 32-bit`
  * `Scipy 32-bit`
  * `Matplotlib 32-bit` [Optional]


* Download OpenCV3
* Extract
* Go to `opencv-3.0.0/opencv/sources/cmake/`
* Open the file in a code editor `OpenCVCompilerOptions.cmake`
* Find this line -> `add_extra_compiler_option(-Werror=non-virtual-dtor)`
* Now add a hash before the line and then save the file [So it would look like this `#add_extra_compiler_option(-Werror=non-virtual-dtor)`]
* Open Cmake in admin mode
* Select the source file and create a destination folder for library binary files [e.g `opencv3`]
* Click configure
* Select `MinGW Makefiles`from option then click next
* Now select specify native compilers
* Select the Qt `gcc` and `g++` compilers [make sure the MinGW from qt is in the Environment variable]
* Click configure again [?]
* Check the + signed option and uncheck the - signed options
  * + WITH_QT
  * + select the python directories
  * - WITH_IPP
* Now Configure again [Until Red highlighting goes away]
* Now Generate
* After generating is done without error go to the `opencv3` directory or the directory you've just built the library into
* Open a CMD on that directory
* Enter the command `mingw32-make`
* After all the process is done now enter the following command `mingw32-make install`
* Now copy the `cv2.pyd` file from `C:\opencv-3.0.0\opencv\build\python\2.7\x86` to `C:\Python27\Lib\site-packages`
* Add the following variables in the environment path 
```c:\users\manash\appdata\local\enthought\canopy\user\scripts;
C:\Program Files (x86)\Microsoft VS Code\bin;
C:\Qt\Qt5.5.1\Tools\mingw492_32\bin;
C:\Users\Manash\AppData\Local\atom\bin;C:\Python27;
C:\Qt\Qt5.5.1\5.5\mingw492_32\bin;
C:\Qt\Qt5.5.1\Tools\mingw492_32\bin;
C:\opencv3\bin;`
```
* Open python CLI and write this line and then press enter `import cv2`
* If nothing shows then you've installed opencv correctly both in qt and python


  
