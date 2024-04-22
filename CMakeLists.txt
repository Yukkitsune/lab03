cmake_minimum_required(VERSION 3.13)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(builder)
include_directories(formatter_ex_lib)
include_directories(formatter_lib)
include_directories(solver_lib)
add_subdirectory(formatter_ex_lib)
add_subdirectory(formatter_lib)
add_subdirectory(solver_lib)

add_executable(hello_world hello_world_application/hello_world.cpp)
add_executable(equation solver_application/equation.cpp)

target_link_libraries(formatter_ex formatter)
target_link_libraries(hello_world formatter_ex)
target_link_libraries(equation formatter_ex)
target_link_libraries(equation solver)

