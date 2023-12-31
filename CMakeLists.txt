cmake_minimum_required(VERSION 3.27)
project(TopDown)

set(CMAKE_CXX_STANDARD 17)

find_package(raylib 3.0) # Let CMake find the raylib package

add_executable(TopDown main.cpp)

if (raylib_FOUND) # If raylib is found
    include_directories(${raylib_INCLUDE_DIRS}) # Include raylib headers
    target_link_libraries(TopDown ${raylib_LIBRARIES}) # Link raylib to your project
endif ()