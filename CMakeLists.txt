cmake_minimum_required(VERSION 3.12)
project(TensorGo)
message(STATUS "root This is BINARY dir " ${PROJECT_BINARY_DIR})
message(STATUS "root This is SOURCE dir " ${PROJECT_SOURCE_DIR})
include_directories(${PROJECT_SOURCE_DIR}/operations
                    ${PROJECT_SOURCE_DIR}/include)
LINK_DIRECTORIES(
        ${PROJECT_BINARY_DIR}/lib)
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)
SET(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/lib)

add_subdirectory(operations)
add_subdirectory(file_system)
add_subdirectory(samples)
add_subdirectory(tensor)
add_subdirectory(util)