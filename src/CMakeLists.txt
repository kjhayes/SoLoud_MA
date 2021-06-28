cmake_minimum_required(VERSION 3.19)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -msse4.1")

file(GLOB SRC_FILES "${CMAKE_CURRENT_SOURCE_DIR}/*.cpp" "${CMAKE_CURRENT_SOURCE_DIR}/*.c")
add_library(${CMAKE_PROJECT_NAME} STATIC ${SRC_FILES})

target_compile_definitions(${CMAKE_PROJECT_NAME} PUBLIC -DWITH_MINIAUDIO)
target_include_directories(${CMAKE_PROJECT_NAME} PUBLIC "${CMAKE_SOURCE_DIR}/include/SoLoud")