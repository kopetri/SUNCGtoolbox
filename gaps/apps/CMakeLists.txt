cmake_minimum_required (VERSION 3.8)

project (img2img)
project (scn2cam)
project (scn2grd)
project (scn2img)
project (scn2scn)
project (scninfo)
project (scnview)


add_executable(img2img img2img/img2img.cpp)
target_link_libraries(img2img gaps) 

add_executable(scn2cam scn2cam/scn2cam.cpp)
target_link_libraries(scn2cam gaps) 

add_executable(scn2grd scn2grd/scn2grd.cpp)
target_link_libraries(scn2grd gaps) 

add_executable(scn2img scn2img/scn2img.cpp)
target_link_libraries(scn2img gaps) 

add_executable(scn2scn scn2scn/scn2scn.cpp)
target_link_libraries(scn2scn gaps) 

add_executable(scninfo scninfo/scninfo.cpp)
target_link_libraries(scninfo gaps) 

add_executable(scnview scnview/scnview.cpp)
target_link_libraries(scnview gaps) 