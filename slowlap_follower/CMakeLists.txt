cmake_minimum_required(VERSION 3.0.2)
project(slowlap_follower)


find_package(catkin REQUIRED COMPONENTS
  roscpp
  nav_msgs
  geometry_msgs
  std_msgs
  mur_common
)

add_definitions(-std=c++14)
include_directories(src ${catkin_INCLUDE_DIRS})
catkin_package()

add_executable(slowlap_follower src/follower.cpp)

target_link_libraries(slowlap_follower ${catkin_LIBRARIES})





