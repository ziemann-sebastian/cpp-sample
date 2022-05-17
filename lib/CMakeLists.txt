cmake_minimum_required(VERSION 3.10)

set(CMAKE_CXX_STANDARD 14)

# set the project name
project(samplelib VERSION 1.0.0)

# Add a shared library
add_library(samplelib SHARED SampleLib.cpp)

# Add include dir
include_directories(${CMAKE_CURRENT_SOURCE_DIR})

# Set the version property.
set_target_properties(${PROJECT_NAME} PROPERTIES VERSION ${PROJECT_VERSION})

# Set the shared object version property to the project's major version.
set_target_properties(${PROJECT_NAME} PROPERTIES SOVERSION ${PROJECT_VERSION_MAJOR})

# Install header and library
install(TARGETS samplelib DESTINATION lib)
install(FILES SampleLib.h DESTINATION include)
