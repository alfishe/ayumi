# Minimum version of CMake required to build the project
cmake_minimum_required(VERSION 3.10)

# Project name
project(ayumi)

# Set the C++ standard to C++17
set(CMAKE_CXX_STANDARD 17)

# Set the C standard to C11
set(CMAKE_C_STANDARD 11)

# Add the source files to the project
set(SOURCES
    src/ayumi.c
    src/ayumi.h
    src/ayumi_render.c
    src/load_text.c
    src/load_text.h
)

# Create the executable target
add_executable(${PROJECT_NAME} ${SOURCES})

# Executable will be generated with 'ayumi_render' name
set_target_properties(${PROJECT_NAME} PROPERTIES OUTPUT_NAME "ayumi_render")


# Set any additional compiler flags
target_compile_options(${PROJECT_NAME} PRIVATE -Wall -Wextra)
