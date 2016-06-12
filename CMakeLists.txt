##############################################################################
# CMake
##############################################################################

cmake_minimum_required(VERSION 2.8.3)
project(smarthome_light_msgs_java)

##############################################################################
# Catkin
##############################################################################

find_package(catkin REQUIRED genjava geometry_msgs sensor_msgs smarthome_msgs smarthome_light_msgs)

generate_rosjava_messages(
  PACKAGES
    smarthome_light_msgs
)

catkin_package()

##############################################################################
# Installation
##############################################################################

install(DIRECTORY ${CATKIN_DEVEL_PREFIX}/${CATKIN_GLOBAL_MAVEN_DESTINATION}/org/ros/rosjava_messages/
        DESTINATION ${CATKIN_GLOBAL_MAVEN_DESTINATION}/org/ros/rosjava_messages)
