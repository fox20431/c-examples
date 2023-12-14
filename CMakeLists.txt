cmake_minimum_required(VERSION 3.0)

project(c_examples)

set(CMAKE_BINARY_DIR ${CMAKE_SOURCE_DIR}/build)

set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)
set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR}/lib)

add_executable(hello_world hello_world.c)
add_executable(xor xor.c)

add_custom_target(run
    COMMAND ${EXECUTABLE_OUTPUT_PATH}/myapp
    DEPENDS myapp
    WORKING_DIRECTORY ${EXECUTABLE_OUTPUT_PATH}
)