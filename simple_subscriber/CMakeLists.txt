cmake_minimum_required(VERSION 3.5)
project(simple_subscriber)

find_package(ament_cmake REQUIRED)
find_package(rclcpp      REQUIRED)
find_package(std_msgs    REQUIRED)

add_executable(listener src/listner.cpp)
ament_target_dependencies(listener rclcpp std_msgs)

install(TARGETS listener DESTINATION lib/${PROJECT_NAME})

ament_package()
