project(EventVisionLibrary)
cmake_minimum_required(VERSION 3.1)

set(CMAKE_MACOSX_RPATH 1)

# set c++11
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall -pthread")

# cmake can locate ${CMAKE_PREFIX_PATH}/lib
set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)
SET(CMAKE_RUNTIME_OUTPUT_DIRECTORY ../)

include("CMakeLists.shared")

add_subdirectory("save_csv")
add_subdirectory("shutdown")
add_subdirectory("stream_event")
add_subdirectory("rodtracking")

# if you want to install this, you need to install OpenGL.
# In the minimal configuration, we don't need OpenGL.
#add_subdirectory("rodtracking_gl")
