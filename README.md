# RoboND-Map-My-World-Robot
Udacity Robotics Software Engineer Nanodegree Term 2 Project: Map My World:

RTAB-Map is the best solution for SLAM to develop robots that can map environments in 3D. These considerations come from RTAB-Map's speed and memory management, its custom developed tools for information analysis and, most importantly, the quality of the documentation. Being able to leverage RTAB-Map with our own robots will lead to a solid foundation for mapping and localization well. For this project we will be using the rtabmap_ros package, which is a ROS wrapper (API) for interacting with rtabmap. 

### Running the Scripts
Run the following commands below in separate terminals:  
Launch the world in Gazebo:  
``roslaunch slam_project world.launch world_file:=~/catkin_ws/src/slam_project/worlds/kitchen_dining.world``  
Launch the teleop node for keyboard control:  
``roslaunch slam_project teleop.launch``  
Launch the RTAB-Map mapping node  
``roslaunch slam_project mapping.launch``  
Launch the RViz GUI:  
``roslaunch slam_project rviz.launch``  

### Future Work - Applies RTAB Mapping to a real robot

Intel aero flying car      | RTAB-Map
:-------------------------:|:-------------------------:
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/qXfB4bgf53A/0.jpg)](https://youtu.be/qXfB4bgf53A) |  [![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/rF9DJFgUhv0/0.jpg)](https://youtu.be/rF9DJFgUhv0) 

