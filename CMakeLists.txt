cmake_minimum_required(VERSION 3.20)

project(proga)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)
set_property(GLOBAL PROPERTY PREDEFINED_TARGETS_FOLDER "cmake")
set_property(GLOBAL PROPERTY CXX_STANDARD 20)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_subdirectory(src)
include_directories(src)