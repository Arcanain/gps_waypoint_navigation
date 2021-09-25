cmake_minimum_required(VERSION 3.0.2)
project(gps_waypoint_navigation)

set(CMAKE_CXX_FLAGS "-std=c++11")
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_C_STANDARD 11)

find_package(catkin REQUIRED
    roscpp
    rospy
    std_msgs
    tf
    roslib
    roslaunch
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES gps_waypoint_navigation
   CATKIN_DEPENDS tf
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

add_executable(gps_waypoint src/gps_waypoint.cpp)
target_link_libraries(gps_waypoint ${catkin_LIBRARIES})