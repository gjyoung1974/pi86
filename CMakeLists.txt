# Set up a C++ Project
cmake_minimum_required(VERSION 3.16.3)
project(pi86)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_VERBOSE_MAKEFILE ON)

set(CMAKE_CXX_FLAGS "-Wno-narrowing")

# Include headers
include_directories(.)

# Set up the executable
add_executable(pi86 pi86.cpp x86.cpp vga.cpp font.h timer.cpp drives.cpp keycodes.h)

# find required packages
find_package(SDL2 REQUIRED)
find_package(Threads REQUIRED)
find_library(WIRINGPI_LIBRARIES NAMES wiringPi)
find_library(PIGPIO_LIBRARIES NAMES pigpio)

# Link it
target_link_libraries(pi86 ${WIRINGPI_LIBRARIES})
target_link_libraries(pi86 ${CMAKE_THREAD_LIBS_INIT})
target_link_libraries(pi86 ${SDL2_LIBRARIES} )
target_link_libraries(pi86 ${PIGPIO_LIBRARIES} )
