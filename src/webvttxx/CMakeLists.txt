cmake_minimum_required(VERSION 3.1 FATAL_ERROR)


add_library(libwebvttxx STATIC
        abstract_parser.cpp
        file_parser.cpp)

target_include_directories(libwebvttxx PUBLIC
        "${PROJECT_SOURCE_DIR}/include")


# prevent the output file from being named something like "liblibwebvttxx.a"
set_target_properties(libwebvttxx PROPERTIES PREFIX "")