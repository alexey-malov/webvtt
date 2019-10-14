cmake_minimum_required(VERSION 3.1 FATAL_ERROR)

# Set project information
project(LibWebVTT VERSION 1.0.0 LANGUAGES C CXX)
set(PROJECT_BRIEF "A cross-platform implementation of a WebVTT parser written in C and C++")
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)

SET(GCC_COVERAGE_COMPILE_FLAGS "-Wno-narrowing")
SET(CMAKE_CXX_FLAGS  "${CMAKE_CXX_FLAGS} ${GCC_COVERAGE_COMPILE_FLAGS}")


add_subdirectory("src")
add_subdirectory("test")
