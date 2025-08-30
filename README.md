## HelloCMAKE

The simplest program built using CMake in the bash terminal.

1.) Create a main.cpp file in the project directory.

2.) Create a CMakeLists.txt file in the project directory and copy this text: (Modify for your project)

    cmake_minimum_required(VERSION 3.10)
    set(CMAKE_CXX_STANDARD 17)
    set(CMAKE_CXX_STANDARD_REQUIRED ON)
    
    project(HelloCMake VERSION 1.0)
    add_executable(HelloCMake main.cpp)

    #target_include_directories(HelloCMake PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

3.) Build with CMake from the cli:

    - cmake .      (run cmake from the current directory)
    - make         (run the make file that cmake created)
    - ./HelloCmake (run the program executable created by the make file)

## Next Level Hello

4.) Add an 'include' and 'build' directories to the project directory.

5.) Add 'main.h' to the 'include' directory and use the 'target_include_directories' in 'CMakeLists.txt'.

6.) Remove all old build files and directories so that only the main.cpp and CMakeLists.txt are in the root directory.

7.) Build from the build folder:

    - cd build
    - cmake ..
    - make

8.) Run program from project directory:

    - ./build/HelloCMake
