cmake_minimum_required(VERSION 3.0.2)
project(panthera_gazebo)

find_package(catkin REQUIRED COMPONENTS
  gazebo_ros
)

catkin_package(
  CATKIN_DEPENDS gazebo_ros
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

install(DIRECTORY launch models worlds
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)