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

This package contains a main launch file launching all the required launch files in a go.

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
On 1st Terminal
````
roslaunch ardupilot_ros gzbo.launch #for quadrotor
````
or
````
roslaunch ardupilot_ros gzbo_rover.launch #for rover
````

On 2nd Terminal
````
../Tools/autotest/sim_vehicle.py -f gazebo-iris
````
or
````
sim_vehicle.py -v APMrover2 -f gazebo-rover -m --mav10 -I1
````

On 3rd Terminal
````
roslaunch ardupilot_ros main.launch
````
