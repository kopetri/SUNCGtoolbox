cmake_minimum_required (VERSION 3.8)

project (png)

file(GLOB_RECURSE png_SRCS *.c)
file(GLOB_RECURSE png_HDRS *.h)


add_library(png ${png_SRCS} ${png_HDRS})
target_include_directories(png PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
set_target_properties( png
  PROPERTIES
  ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib"
  LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib"
  RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin"
)