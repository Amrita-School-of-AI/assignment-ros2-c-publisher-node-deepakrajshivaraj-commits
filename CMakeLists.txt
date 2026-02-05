cmake_minimum_required(VERSION 3.8)
project(assignment-ros2-c-publisher-node-deepakrajshivaraj-commits)

if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 17)
endif()

find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)
find_package(std_msgs REQUIRED)

add_executable(publisher_node src/publisher_node.cpp)
ament_target_dependencies(publisher_node rclcpp std_msgs)

install(TARGETS
  publisher_node
  DESTINATION lib/${PROJECT_NAME}
)

ament_package()
