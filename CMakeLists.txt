cmake_minimum_required(VERSION 3.5)
project(robotic_setups_description)

# If you build C++ code, set a standard
if(NOT CMAKE_CXX_STANDARD)
    set(CMAKE_CXX_STANDARD 14)
endif()

find_package(ament_cmake REQUIRED)
# find_package(rclcpp REQUIRED)                 # uncomment if you have rclcpp nodes
# find_package(ament_index_cpp REQUIRED)        # example extra dependencies

# Add libraries / executables here, for example:
# add_executable(my_node src/my_node.cpp)
# ament_target_dependencies(my_node rclcpp std_msgs)
# install(TARGETS my_node DESTINATION lib/${PROJECT_NAME})

# Install non-code resources (URDFs, meshes, launch files etc.)
install(
    DIRECTORY launch urdf meshes config
    DESTINATION share/${PROJECT_NAME}
)

ament_package()