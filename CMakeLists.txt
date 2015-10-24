cmake_minimum_required(VERSION 3.3)

set(CMAKE_CXX_COMPILER clang++)

project(modules)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -fmodules -fmodules-cache-path=${CMAKE_SOURCE_DIR}/cache")

# if you have libc++
# set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -stdlib=libc++")

set(SOURCE_FILES
    src/main.cpp
    src/Awesome/Awesome.hpp
    src/Awesome/Awesome.cpp)
add_executable(modules ${SOURCE_FILES})
