cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

# Find Eigen
find_package(Eigen3 REQUIRED)
include_directories(${EIGEN3_INCLUDE_DIRS})


# Find Gazebo
find_package(gazebo REQUIRED)
include_directories(${GAZEBO_INCLUDE_DIRS})
link_directories(${GAZEBO_LIBRARY_DIRS})
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${GAZEBO_CXX_FLAGS}")

# Build our plugin
add_library(usv_dynamics_plugin SHARED gazebo_usv_dynamics_plugin.cpp)
target_link_libraries(usv_dynamics_plugin ${GAZEBO_LIBRARIES})