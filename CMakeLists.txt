
cmake_minimum_required( VERSION 2.8 )
project( homography )

set( CMAKE_CXX_FLAGS "-std=c++14" )

find_package( OpenCV 4.2 REQUIRED )

include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable( virtualBillboard virtual-billboard.cpp )

target_link_libraries( virtualBillboard ${OpenCV_LIBS} )