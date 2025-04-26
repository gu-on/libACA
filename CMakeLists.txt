cmake_minimum_required(VERSION 3.15)

project(ACA VERSION 0.3.1 LANGUAGES CXX C)

set(ACA_SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR})

list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake")

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

configure_file(${ACA_SOURCE_DIR}/src/${PROJECT_NAME}Config.h.in ${CMAKE_BINARY_DIR}/inc/${PROJECT_NAME}Config.h)

add_subdirectory(3rdparty/Fft)
add_subdirectory(3rdparty/sndlib)
add_subdirectory(src/ACA)
add_subdirectory(src/AudioFileIO)

enable_testing()
add_subdirectory(test)