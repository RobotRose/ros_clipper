cmake_minimum_required(VERSION 2.8.3)
project(ros_clipper)

catkin_package(
    INCLUDE_DIRS include
    LIBRARIES polyclipping
#    CATKIN_DEPENDS
#    DEPENDS 
)

include_directories(
	${PROJECT_SOURCE_DIR}/include
)

add_library(polyclipping SHARED ${PROJECT_SOURCE_DIR}/src/clipper.cpp)
target_link_libraries(polyclipping ${catkin_LIBRARIES})