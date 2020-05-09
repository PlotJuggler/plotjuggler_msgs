cmake_minimum_required(VERSION 3.5)
project(pj_msgs_ejample)

# Default to C++14
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 14)
endif()

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)
find_package(pj_msgs REQUIRED)


add_executable(test_plotjuggler_msgs example.cpp)
ament_target_dependencies(test_plotjuggler_msgs rclcpp pj_msgs)

install(TARGETS test_plotjuggler_msgs
  DESTINATION bin
)

ament_package()
