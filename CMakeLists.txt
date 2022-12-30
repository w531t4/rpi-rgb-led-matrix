cmake_minimum_required(VERSION 3.7.2)
set (CMAKE_CXX_STANDARD 11)
if(NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Release)
endif()

if (CMAKE_BUILD_TYPE STREQUAL "Debug")
    set(CMAKE_VERBOSE_MAKEFILE on)
endif(CMAKE_BUILD_TYPE STREQUAL "Debug")

set(CMAKE_C_FLAGS "-Wall -Wextra")
set(CMAKE_C_FLAGS_DEBUG "-g")
set(CMAKE_C_FLAGS_RELEASE "-O3")

set(CMAKE_CXX_FLAGS "-Wall -Wextra")
set(CMAKE_CXX_FLAGS_DEBUG "-g")
set(CMAKE_CXX_FLAGS_RELEASE "-O3")

#set(HARDWARE_DESC "regular")
#set(INVERSE_RGB_DISPLAY_COLORS)
#set(SHOW_REFRESH_RATE)
#set(RGB_SCAN_INTERLACED "1")
#set(RGB_SLOWDOWN_GPIO "1")
#set(LSB_PWM_NANOSECONDS "130")
#set(DISABLE_HARDWARE_PULSES)
#set(REMOVE_DEPRECATED_TRANSFORMERS)

# experimental
#set(FIXED_FRAME_MICROSECONDS "5000")
#set(ONLY_SINGLE_SUB_PANEL)

#set(USER_DEFINES "-DBLAH=1")

project(rpirgbledmatrix)

add_subdirectory("lib")
add_subdirectory("examples-api-use")
