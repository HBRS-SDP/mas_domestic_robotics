cmake_minimum_required(VERSION 2.8.3)
project(mdr_demo_simple_pick_and_place)

find_package(catkin REQUIRED COMPONENTS
  roslint
  rospy
  smach_ros
  smach
  actionlib
  mongodb_store
  mdr_rosplan_interface
  mas_execution_manager
  mdr_move_base_action
  mdr_move_arm_action
  mdr_pickup_action
  mdr_place_action
  mdr_perceive_plane_action
)

catkin_package(
  CATKIN_DEPENDS
    roslint
    rospy
    smach_ros
    smach
    actionlib
    mongodb_store
    mdr_rosplan_interface
    mas_execution_manager
    mdr_move_base_action
    mdr_move_arm_action
    mdr_pickup_action
    mdr_place_action
    mdr_perceive_plane_action
)

catkin_python_setup()
roslint_python()

install(DIRECTORY ros/launch/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/ros/launch
)
