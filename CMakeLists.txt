cmake_minimum_required(VERSION 3.20)
project(vulkan-sandbox LANGUAGES C CXX)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# C++ version and std
if(NOT DEFINED CMAKE_CXX_STANDARD)
    set(CMAKE_CXX_STANDARD 20)
    set(CMAKE_CXX_STANDARD_REQUIRED ON)
endif()

# Vulkan
find_package(Vulkan REQUIRED)

# externals
add_subdirectory("externals/")

# vkl
add_subdirectory("vkl/")

# sandbox
add_subdirectory("sandbox/")