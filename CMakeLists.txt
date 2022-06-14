cmake_minimum_required(VERSION 3.5)
project(hdr)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -msse4.1")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -msse4.1")

find_package(OpenMP REQUIRED)
message("-- OPENMP FOUND")
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} ${OpenMP_C_FLAGS}")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${OpenMP_CXX_FLAGS}")


add_subdirectory(Layer)
add_subdirectory(Mat)
add_subdirectory(ISPpipeline)
