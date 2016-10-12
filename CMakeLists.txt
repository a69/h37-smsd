cmake_minimum_required(VERSION 3.6)
project(h37_smsd)
set (SMSD_VERSION_MAJOR 1)
set (SMSD_VERSION_MINOR 0)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

include_directories("${PROJECT_BINARY_DIR}")
include_directories("/usr/include/gammu")


set(SOURCE_FILES main.c)
add_executable(h37_smsd ${SOURCE_FILES})
target_link_libraries(h37_smsd Gammu gsmsd)