cmake_minimum_required(VERSION 3.10)
project(dyad C)

add_library(dyad src/dyad.c)

IF (WIN32)
    target_link_libraries(dyad ws2_32)
ENDIF ()

target_include_directories(dyad PRIVATE src)
