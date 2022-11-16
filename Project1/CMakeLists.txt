# For more information about using CMake with Android Studio, read the
# documentation: https://d.android.com/studio/projects/add-native-code.html

# Sets the minimum version of CMake required to build the native library.

cmake_minimum_required(VERSION 3.18.1)

# Declares and names the project.

project("Project1")

# Project Folders
# include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../include/app)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O3 -Wall -shared -std=c++11 -fPIC -I/usr/include/python3.10 -lpython3.10")

add_executable( # Sets the name of the library.
        Project1

        # Provides a relative path to your source file(s).
        ${CMAKE_CURRENT_SOURCE_DIR}/main.cpp
        )

# end_of_file
