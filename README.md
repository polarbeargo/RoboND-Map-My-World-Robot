# RoboND-Map-My-World-Robot
Udacity Robotics Software Engineer Nanodegree Term 2 Project: Map My World:

RTAB-Map 's speed and memory management is the best solution for SLAM to develop robots and map environments in 3D for information analysis and the quality of the documentation. Being able to leverage RTAB-Map with our own robots will lead to a solid foundation for mapping and localization well. For this project, we will use the rtabmap_ros package, which is a ROS wrapper (API) for interacting with rtabmap. 

### Running the Scripts

Create folder and Load model:
```
mkdir ~/.gazebo
curl -L https://s3-us-west-1.amazonaws.com/udacity-robotics/Term+2+Resources/P3+Resources/models.tar.gz | tar zx -C ~/.gazebo/

```
Run the following commands below in separate terminals:  
Launch the world in Gazebo:  
```
catkin_make
source devel/setup.bash 
roslaunch slam_project world.launch world_file:=~/catkin_ws/src/slam_project/worlds/kitchen_dining.world
```  
Launch the teleop node for keyboard control:  
```
catkin_make
source devel/setup.bash 
roslaunch slam_project teleop.launch 
```
Launch the RTAB-Map mapping node  
```
catkin_make
source devel/setup.bash 
roslaunch slam_project mapping.launch
```  
Launch the RViz GUI:  
```
catkin_make
source devel/setup.bash 
roslaunch slam_project rviz.launch
``` 
### Or use rtab_run script
```
cd /home/workspace/catkin_ws
source devel/setup.bash
cd src/slam_project/scripts
./rtab_run
```

### Future Work - Applies RTAB Mapping to a real robot

Intel aero flying car      | RTAB-Map
:-------------------------:|:-------------------------:
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/qXfB4bgf53A/0.jpg)](https://youtu.be/qXfB4bgf53A) |  [![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/rF9DJFgUhv0/0.jpg)](https://youtu.be/rF9DJFgUhv0) 

