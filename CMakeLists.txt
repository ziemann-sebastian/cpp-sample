cmake_minimum_required(VERSION 3.10)

# set the project name
project(cpp_sample)

# add the executable
add_executable(cpp_sample main.cpp)

# Install into ${prefix}/bin
install(TARGETS cpp_sample DESTINATION bin)
