cmake_minimum_required(VERSION 3.19)
project(net1)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories("dependencies/asio-1.18.2/include/")


file(GLOB_RECURSE SRC_FILES source/*.cpp)
add_executable(net1 main.cpp ${SRC_FILES})
target_link_libraries(net1 -lpthread)
