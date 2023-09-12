# Minimum required version of CMake
cmake_minimum_required(VERSION 3.0)

# Project name
project(hello_slam)

# Add source files to the project
add_executable(hello_slam hello_slam.cpp)
add_library(hello_shared SHARED lib_hello_slam.cpp)

add_executable(use_hello use_hello.cpp )
target_link_libraries(use_hello hello_shared)