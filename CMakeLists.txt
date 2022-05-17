cmake_minimum_required(VERSION 3.10)

set(CMAKE_CXX_STANDARD 14)

# set the project name
project(cpp_sample)

# add the executable
add_executable(cpp_sample main.cpp)

target_link_libraries(cpp_sample samplelib)

# Install into ${prefix}/bin
install(TARGETS cpp_sample DESTINATION bin)
