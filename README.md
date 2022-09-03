# ardupilot_ros package for non-gps navigation

## Description : 
This is a ROS package for non-gps navigation for ardupilot containing all the required files and listed dependencies. This also contains a file from <thien94/vision_to_mavros> to set origin. This package contains all the modified files for the following packages:
````
mavros
cartographer_ros
robot_pose_publisher
````


## Requirements :
Ubuntu version 18.04 or 20.04

ROS Melodic or Noetic

## Usage :

This package contains a central launch file launching all the required launch files in a go.

Simply,

````
cd <ros_ws>/src/
git clone https://github.com/snktshrma/ardupilot_ros
cd ..
rosdep install --from-paths src --ignore-src -r -y
cd ardupilot_ros
catkin build
````

Then,
````
roslaunch ardupilot_ros main.launch
````
