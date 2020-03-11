cmake_minimum_required(VERSION 2.8.3)
project(pilz_industrial_motion_testutils)

find_package(catkin REQUIRED)

############
## python ##
############
catkin_python_setup()

###################################
## catkin specific configuration ##
###################################
catkin_package()

##################
## installation ##
##################
install(PROGRAMS
   src/${PROJECT_NAME}/xml_testdata_loader.py
   src/${PROJECT_NAME}/acceptance_test_utils.py
   DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(DIRECTORY
   test_data
   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)