cmake_minimum_required(VERSION 3.10.2)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -msse4.1")

file(GLOB SRC_FILES "${CMAKE_CURRENT_SOURCE_DIR}/*.cpp" "${CMAKE_CURRENT_SOURCE_DIR}/*.c")
add_library(${SOLOUD_MA_LIB_NAME} STATIC ${SRC_FILES})

target_compile_definitions(${SOLOUD_MA_LIB_NAME} PUBLIC -DWITH_MINIAUDIO)
target_include_directories(${SOLOUD_MA_LIB_NAME} PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/../include/SoLoud")
