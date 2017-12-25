cmake_minimum_required(VERSION 2.8.3)

include(cmake/HunterGate.cmake)
HunterGate(
    URL "https://github.com/lsolanka/hunter/archive/v0.19.210-4.tar.gz"
    SHA1 "2b18594936d8faded8c59b0a33567af47f50bdb4"
)

project(message_runtime)

hunter_add_package(ros-catkin)
hunter_add_package(ros-roscpp_core)

find_package(catkin REQUIRED)

catkin_package(CATKIN_DEPENDS cpp_common roscpp_serialization roscpp_traits rostime)
