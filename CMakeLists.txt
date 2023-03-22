cmake_minimum_required(VERSION 3.20.3)
set (CMAKE_CXX_STANDARD 11)

project(Adventure)

add_executable (AdventureExe src/main.cpp)

add_library(Engine)

# Link the executable to the library
target_link_libraries (AdventureExe Engine)

# Specify subfolders of the library
add_subdirectory(src)
add_subdirectory(include)

# A folder to search through when looking for includes
include_directories(${CMAKE_SOURCE_DIR}/include)
