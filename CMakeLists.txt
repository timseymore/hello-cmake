cmake_minimum_required(VERSION 3.10)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(HelloCMake VERSION 1.0)
add_executable(HelloCMake main.cpp)

target_include_directories(HelloCMake PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
