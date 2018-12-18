cmake_minimum_required (VERSION 3.8)

project (jpeg)

file(GLOB_RECURSE jpeg_SRCS *.c)
file(GLOB_RECURSE jpeg_HDRS *.h)

add_library(jpeg ${jpeg_SRCS} ${jpeg_HDRS})
target_include_directories(jpeg PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
set_target_properties( jpeg
  PROPERTIES
  ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib"
  LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib"
  RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin"
)