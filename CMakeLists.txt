cmake_minimum_required(VERSION 2.8.9)
project(fft)

#Bring the headers 
include_directories(include)

#Can manually add the sources using the set command as follows:
#set(SOURCES src/mainapp.cpp src/Student.cpp)

#However, the file(GLOB...) allows for wildcard additions:
file(GLOB SOURCES "src/*.c")

add_executable(fft ${SOURCES})
#target_link_libraries()
target_link_libraries(fft m)
set(CMAKE_BUILD_TYPE Debug)
