# HelloCMAKE

### The simplest program built using CMake in the bash terminal.

> To recreate this repo for your starter project, follow this procedure:

1. Create a `main.cpp` file in the project directory and add the following code.

       #include <iostream>

        int main ()
        {
          std::cout << "Hello Cmake!" << std::endl;
          return 0;
        }

3. Create a CMakeLists.txt file in the project directory and copy this text: (Modify for your project)

        cmake_minimum_required(VERSION 3.10)
        
        set(CMAKE_CXX_STANDARD 17)
        
        set(CMAKE_CXX_STANDARD_REQUIRED ON)
       
        project(HelloCMake VERSION 1.0)
        
        add_executable(HelloCMake main.cpp)

4. Build with CMake from the CLI:

    - Run CMake from the current directory using `cmake . `
    - Run the MakeFile that CMake created using `make`
    - Run the program executable created by the MakeFile with `./HelloCMake`

## Next Level Hello

4. Add an `include` and `build` directories to the project directory.

5. Add `main.h` to the `include` directory and add this code.

        #pragma once
   
        #include <iostream>
   
7. Change the include statement in `main.cpp` to `#include "main.h"`.
   
8. Add the `target_include_directories` function in `CMakeLists.txt`.

    `target_include_directories(HelloCMake PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)`

9. Remove all old build files and directories so that only the `main.cpp` and `CMakeLists.txt` are in the root directory.

10. Build from the build folder.

    - `cd build`
    - `cmake ..`
    - `make`

11. Run the program from the project directory.

    `./build/HelloCMake`
