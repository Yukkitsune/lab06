
cmake_minimum_required(VERSION 3.13)
project(hello_world)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories("../formatter_ex_lib/")

add_executable(hello_world hello_world.cpp)

add_subdirectory("../formatter_ex_lib/" formatter_ex)

target_link_libraries(hello_world formatter_ex)
target_include_directories(hellow_world PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
