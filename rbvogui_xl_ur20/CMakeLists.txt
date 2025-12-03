cmake_minimum_required(VERSION 3.5)
project(rbvogui_xl_ur20)

find_package(ament_cmake REQUIRED)

#install(DIRECTORY include/
#  DESTINATION include/${PROJECT_NAME}
#)

install(FILES
  shrxl-250502ab.xacro
  DESTINATION share/${PROJECT_NAME}
)

ament_package()