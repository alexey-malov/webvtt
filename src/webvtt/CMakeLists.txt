cmake_minimum_required(VERSION 3.1 FATAL_ERROR)

add_definitions("-DACSDK_LOG_MODULE=captionslib")
add_library(libwebvtt STATIC
        alloc.c
        cue.c
        cuetext.c
        error.c
        lexer.c
        node.c
        parser.c
        string.c)

target_include_directories(libwebvtt PUBLIC
        "${libwebvtt_SOURCE_DIR}"
        "${PROJECT_SOURCE_DIR}/include")

# prevent the output file from being named something like "liblibwebvtt.a"
set_target_properties(libwebvtt PROPERTIES PREFIX "")