cmake_minimum_required(VERSION 3.13)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(print)
include_directories(formatter_ex_lib)
include_directories(formatter_lib)
add_subdirectory(formatter_ex_lib)
add_subdirectory(formatter_lib)

target_link_libraries(formatter_ex formatter)

