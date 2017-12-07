cmake_minimum_required(VERSION 2.8.3)

include(cmake/HunterGate.cmake)
HunterGate(
    URL "https://github.com/lsolanka/hunter/archive/4ecf66e071495981031fdfa99aad576405537266.tar.gz"
    SHA1 "727648f578f3cbcb6ea0e644bd8b0111e56688bc"
    LOCAL
)

project(message_runtime)

hunter_add_package(catkin)
hunter_add_package(roscpp_core)

find_package(catkin REQUIRED)

catkin_package(CATKIN_DEPENDS cpp_common roscpp_serialization roscpp_traits rostime)
