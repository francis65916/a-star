cmake_minimum_required (VERSION 2.8.11)
project (a-star)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
set(CMAKE_C_COMPILER "/mingw64/bin/clang.exe")
set(CMAKE_CXX_COMPILER "/mingw64/bin/clang++.exe")
	
include_directories($C_INCLUDE_PATH$ $CPLUS_INCLUDE_PATH$ source)
add_library(a-star source/AStar.cpp)

add_executable(main main.cpp)
target_link_libraries(main a-star)
