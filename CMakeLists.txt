cmake_minimum_required(VERSION 2.8.3)
project(arc_msgs)

find_package(catkin REQUIRED COMPONENTS
  	roscpp
    geometry_msgs
    std_msgs
    message_generation
)

add_message_files(
  FILES
  State.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

include_directories(include ${catkin_INCLUDE_DIRS})
