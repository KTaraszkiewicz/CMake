cmake_minimum_required(VERSION 3.10)
project(MyProject)

set(HEADER_FILES StackMinimum.h)
set(SOURCE_FILES main.cpp StackMinimum.cpp)

add_executable(MyProject ${HEADER_FILES} ${SOURCE_FILES})

target_include_directories(MyProject PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

add_subdirectory(lib)

target_link_libraries(MyProject PRIVATE StackMinimum)