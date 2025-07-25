# ROS2-Humble
A practical hands-on guide to understanding ROS 2 Nodes using the turtlesim simulator.

## Requirements

- ROS 2 Humble installed
- The turtlesim package (comes pre-installed)
- Multiple terminal windows (each node in a separate terminal)
- Always source ROS 2 in every terminal:  source /opt/ros/humble/setup.bash

  ## 1-Launch the turtlesim simulator
  ros2 run turtlesim turtlesim_node
  This opens the turtlesim window and starts a node named: /turtlesim

  ## 2-View active nodes
  ros2 node list
  Expected output: /turtlesim

  ## 3-Control the turtle using keyboard
  Open a new terminal: ros2 run turtlesim turtle_teleop_key

  ## 4-Rename a node using remapping
  Open a new terminal: ros2 run turtlesim turtlesim_node --ros-args --remap __node:=my_turtle

  Now chack all active nodes: ros2 node list
  Output:
  /turtlesim
/teleop_turtle
/my_turtle

## 5-Get detailed node information
ros2 node info /my_turtle
  
  
  
