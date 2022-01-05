cmake_minimum_required(VERSION 3.0.2)
project(panthera_description)

find_package(catkin REQUIRED COMPONENTS
  urdf
)

catkin_package(
  CATKIN_DEPENDS urdf velodyne_simulator
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

install(DIRECTORY rviz meshes urdf launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)