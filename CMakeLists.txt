cmake_minimum_required(VERSION 3.22)
set(CMAKE_CXX_COMPILER /usr/bin/g++)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_EXTENSIONS OFF)

project(IntermediateProject)
# wanna use g++ instead of clang

set(LIBRARY_NAME Library)
set(EXECUTABLE_NAME Executable)

option(COMPILE_EXECUTABLE "Whether to compile the executable" OFF)


add_subdirectory(src)
if (COMPILE_EXECUTABLE)
    add_subdirectory(app)
else()
    message("W/o exe. compiling")
endif()
