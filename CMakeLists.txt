cmake_minimum_required(VERSION 3.0.2)
project(lang_corr_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS 
    actionlib
    actionlib_msgs
    roscpp
    rospy
    geometry_msgs
    sensor_msgs
    std_msgs
)

# catkin_python_setup()

# add_message_files(
#   FILES
#   BoundingBox.msg
# )

add_service_files(
  FILES
  GetFeaturesFromLanguage.srv
  GetEnvImage.srv
  GetEnvObj.srv
  LatteDeformTraj.srv
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
  sensor_msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES ferl_mj
 CATKIN_DEPENDS message_runtime
)
