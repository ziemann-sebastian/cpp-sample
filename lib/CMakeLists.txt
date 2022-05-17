cmake_minimum_required(VERSION 3.10)

set(CMAKE_CXX_STANDARD 14)

# set the project name
project(samplelib)

# Add a shared library
add_library(samplelib SHARED SampleLib.cpp)

# Add include dir
include_directories(${CMAKE_CURRENT_SOURCE_DIR})

# Install header and library
install(TARGETS samplelib DESTINATION lib)
install(FILES SampleLib.h DESTINATION include)
