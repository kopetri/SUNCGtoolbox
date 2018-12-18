cmake_minimum_required (VERSION 3.8)

project (fglut)

file(GLOB_RECURSE glut_SRCS *.c)
file(GLOB_RECURSE glut_HDRS *.h)

add_library(fglut ${glut_SRCS} ${glut_HDRS})
target_include_directories(fglut PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
set_target_properties( fglut
  PROPERTIES
  ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib"
  LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib"
  RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin"
)