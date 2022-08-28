cmake_minimum_required(VERSION 3.5)
project(cmdline LANGUAGES CXX)

option(CMDLINE_ENABLE_TEST "Enable cmdline test" OFF)


add_library(cmdline INTERFACE)

target_include_directories(cmdline
INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/include
)

if(CMDLINE_ENABLE_TEST)
enable_testing()
add_subdirectory(test)
endif()