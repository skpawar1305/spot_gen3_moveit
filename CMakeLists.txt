cmake_minimum_required(VERSION 3.22)
project(spot_gen3_moveit)

find_package(ament_cmake REQUIRED)

install(PROGRAMS
  nodes/follow_aruco.py
  DESTINATION lib/${PROJECT_NAME}
)

install(DIRECTORY launch DESTINATION share/${PROJECT_NAME}
  PATTERN "setup_assistant.launch" EXCLUDE)
install(DIRECTORY config DESTINATION share/${PROJECT_NAME})
install(FILES .setup_assistant DESTINATION share/${PROJECT_NAME})

ament_package()