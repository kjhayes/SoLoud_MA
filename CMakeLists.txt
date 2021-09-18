cmake_minimum_required(VERSION 3.10.2)

project(SoLoud_MA)

set(SOLOUD_MA_LIB_NAME SoLoud_MA)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/src)

install(TARGETS ${SOLOUD_MA_LIB_NAME} LIBRARY)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/SoLoud TYPE INCLUDE)
