# Installing-and-Launching-Robot-Arm-Packages
This repository shows the steps taken to install robot arm packages

*These packages were applied under ROS melodic and Ubuntu 18.04*

# arduino_robot_arm
`
$ cd ~/catkin_ws/src
$ sudo apt install git
$ git clone https://github.com/smart-methods/arduino_robot_arm 
`

# Dependencies
`
$ cd ~/catkin_ws
$ rosdep install --from-paths src --ignore-src -r -y
$ sudo apt-get install ros-melodic-moveit
$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
`
# Compile the package
`
$ catkin_make
`

# Simulation
`
$ roslaunch robot_arm_pkg check_motors.launch
$ roslaunch robot_arm_pkg check_motors_gazebo.launch
$ rosrun robot_arm_pkg joint_states_to_gazebo.py
`
***I need to change the permission using this command: ***
`
$ cd catkin/src/arduino_robot_arm/robot_arm_pkg/scripts
$ sudo chmod +x joint_states_to_gazebo.py

`

## The Result of the installation:
https://user-images.githubusercontent.com/85858256/124050154-a5c7a580-da22-11eb-9891-457b33d122a5.mp4
