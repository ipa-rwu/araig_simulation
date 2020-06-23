cmake_minimum_required(VERSION 2.8.3)
project(araig_gazebo_worlds)

find_package(catkin REQUIRED)

catkin_package()



### INSTALL ###
install(DIRECTORY Media launch test urdf
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

catkin_install_python(PROGRAMS scripts/elevator.py scripts/tf_publisher.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
