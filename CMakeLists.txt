cmake_minimum_required(VERSION 3.5)

project(osgEarthPagedLOD LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_FLAGS "-Wl,--copy-dt-needed-entries")

#find_package(osg REQUIRED COMPONENTS viewer gdal mapnode map)
#find_package(OpenSceneGraph)
#find_library(OSGEARTH_LIBRARY osgearth)
#find_package(OpenSceneGraphEarth)
#find_package(OpenSceneGraph REQUIRED COMPONENTS osgDB osgGA osgUtil osgViewer)
#find_package(osgEarth REQUIRED COMPONENTS osgEarth osgEarthUtil /usr/local/lib64/libosgearth)

#include_directories(${OPENSCENEGRAPH_INCLUDE_DIRS})


#target_link_libraries(osgEarthPagedLOD ${OPENSCENEGRAPH_LIBRARIES} )
#target_link_libraries(osgEarthPagedLOD ${OPENSCENEGRAPHEARTH_LIBRARIES}
#    /usr/local/lib64/libosgearth.so)
#include_directories(${OSGEARTH_LIBRARIES})

add_executable(osgEarthPagedLOD main.cpp)
target_link_libraries(osgEarthPagedLOD
    -losg
    -losgEarth
)
