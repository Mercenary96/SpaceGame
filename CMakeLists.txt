

cmake_minimum_required(VERSION 2.6)

project(asteroids)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${asteroids_SOURCE_DIR}/cmake")

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${asteroids_SOURCE_DIR}/bin)
# remove debug flags for release build
set(CMAKE_C_FLAGS "-g -O0 -v -da -Q -W -Wall -Wextra -pedantic -std=c99 -lm")

find_package(SDL2 REQUIRED)
include_directories(${SDL2_INCLUDE_DIR})

find_package(SDL2_image REQUIRED)
include_directories(${SDL2_IMAGE_INCLUDE_DIR})

find_package(SDL2_mixer REQUIRED)
include_directories(${SDL2_MIXER_INCLUDE_DIR})

add_subdirectory(src)
