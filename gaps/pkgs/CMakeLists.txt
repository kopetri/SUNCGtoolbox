cmake_minimum_required (VERSION 3.8)

project (gaps)

add_subdirectory(jpeg)
add_subdirectory(png)
add_subdirectory(fglut)

find_package(OpenGL)

file(GLOB_RECURSE r2shapes_SRCS R2Shapes/*.cpp)
file(GLOB_RECURSE r2shapes_HDRS R2Shapes/*.h)

file(GLOB_RECURSE r3graphics_SRCS R3Graphics/*.cpp)
file(GLOB_RECURSE r3graphics_HDRS R3Graphics/*.h)

file(GLOB_RECURSE r3shapes_SRCS R3Shapes/*.cpp)
file(GLOB_RECURSE r3shapes_HDRS R3Shapes/*.h)

file(GLOB_RECURSE rnbasics_SRCS RNBasics/*.cpp)
file(GLOB_RECURSE rnbasics_HDRS RNBasics/*.h)



add_library(gaps ${r2shapes_SRCS} ${r2shapes_HDRS} ${r3graphics_SRCS} ${r3graphics_HDRS} ${r3shapes_SRCS} ${r3shapes_HDRS} ${rnbasics_SRCS} ${rnbasics_HDRS})
target_include_directories(gaps PUBLIC ${CMAKE_CURRENT_SOURCE_DIR} ${OPENGL_INCLUDE_DIR})
target_link_libraries(gaps ${OPENGL_LIBRARIES} jpeg png fglut)



