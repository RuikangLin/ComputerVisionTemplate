# Computer Vision Template

Using OpenCV and cmake from [OpenCV tutorial](https://docs.opencv.org/4.x/db/df5/tutorial_linux_gcc_cmake.html), I created this C++ template repository for myself to create more projects.

### Install Dependencies
> I'm using a M1 macbook so make sure [brew](https://brew.sh/) is installed.
>
> Next, install the dependencies using brew.
> ```bash
> brew install opencv cmake
> ```

### CMakeLists.txt setup
> In the CMakeLists.txt,
> 1. make sure the include_directories is connected to opencv's include/opencv4 folder as that's where all the header files are;
> 2. make sure the file & target_link_libraries are connected to all the .dylib and .a files in the opencv's lib folder;
> 3. the add_executable( executable_name file.cpp ) is how you set the executable name and the file you are compiling.

### Compiling and Running the Executable
> Make sure you are in the repository's directory,
> 
> and run the following to compile:
> ```bash
> cmake .
> make
> ```
> To run the executable:
> ```bash
> ./executable_name
> ```
>
> To test out this template, run:
> ```bash
> cmake.
> make
> ./DisplayImage <image.jpg>
> ```
