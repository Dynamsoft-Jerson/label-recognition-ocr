# Label Recognition Samples
DLR ([Dynamsoft Label Recognition](https://www.dynamsoft.com/label-recognition/overview)) C/C++ sample code for `Windows` and `Linux`.

## Version
1.0 Beta

## Requirements
- [Visual Studio](https://www.visualstudio.com/downloads/)
- [CMake](https://cmake.org/download/)
- [Dynamsoft Label Recognition 1.0 Beta](https://www.dynamsoft.com/label-recognition/downloads)
- [OpenCV 4.5.0](https://opencv.org/releases/)

    Configuration for CMake:

    ```
    # Find OpenCV, you may need to set OpenCV_DIR variable
    # to the absolute path to the directory containing OpenCVConfig.cmake file
    # via the command line or GUI
    find_package(OpenCV REQUIRED)
    ```

## License
Get a [free trial license](https://www.dynamsoft.com/customer/license/trialLicense) and save it to `license.txt`.

## Contact Us
https://www.dynamsoft.com/Company/Contact.aspx

## Windows
1. Copy `*.lib` files to `platforms/win/lib` folder and copy `*.dll` files to `platforms/win/bin` folder.

2. Create a build folder:

    ```
    mkdir build
    cd build
    ```

3. Configure the project.

    - Command-line app

        ```
        cmake -DCMAKE_GENERATOR_PLATFORM=x64 ..
        ```

    - GUI App with OpenCV

        ```
        cmake -DCMAKE_GENERATOR_PLATFORM=x64 -DENABLE_OPENCV=TRUE ..
        ```

4. Build and run the app:

    ```
    cmake --build . --config release
    Release\LabelRecognition license.txt
    ```

    ![label recognition OCR](screenshots/label-recognition-ocr.gif)

## Linux
1. Install CMake:

    ```
    sudo apt-get install cmake
    ```

2. Copy `*.so` files to `platforms/linux` folder.
3. Create a build folder:
    
    ```
    mkdir build
    cd build
    ```

4. Configure the project.

    - Command-line app

        ```
        cmake ..
        ```

    - GUI App with OpenCV

        ```
        cmake -DENABLE_OPENCV=TRUE ..
        ```

5. Build and run the app:

    ```
    cmake --build . --config release
    Release\LabelRecognition license.txt
    ```
    
 ## Blog
 [Text Recognition with Dynamsoft's OCR SDK](https://www.dynamsoft.com/codepool/label-recognition-ocr-windows-linux.html)
