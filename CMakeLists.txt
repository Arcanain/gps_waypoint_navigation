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
#  CATKIN_DEPENDS other_catkin_pkg
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)