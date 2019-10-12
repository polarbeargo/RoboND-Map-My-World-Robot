# RoboND-Map-My-World-Robot
Udacity Robotics Software Engineer Nanodegree Term 2 Project: Map My World:

[//]: # (Image References)

[image1]: ./LATEX/databaseViewer.png
[image2]: ./LATEX/rvizMapping.png
[image3]: ./LATEX/suppliedEnvironment.png
[image4]: ./LATEX/HsinBot.png
[image5]: ./LATEX/RViz.png
[image6]: ./LATEX/corner.png
[image7]: ./LATEX/garageViewer.png
[image8]: ./LATEX/sceneWillow.png
[image9]: ./LATEX/willowDBViewer.png
[image10]: ./LATEX/willowRTAB.png
[image11]: ./LATEX/willowgarage.png
[image12]: ./LATEX/willowgarageHsinBot.png  

RTAB-Map 's speed and memory management is the best solution for SLAM to develop robots and map environments in 3D for information analysis and the quality of the documentation. Being able to leverage RTAB-Map with our own robots will lead to a solid foundation for mapping and localization well. For this project, we will use the rtabmap_ros package, which is a ROS wrapper (API) for interacting with rtabmap. This project is intended to be completed in the Udacity Workspace or on Jetson TX2 and might encounter performance issue on personal laptop or the VM. If working on Jetson TX2, you could use `jetson_clocks.sh` script in the home folder to speed it up! 

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
### RTAB-Map Visualization Tools - Databse Viewer  
* After stop mapping.launch in terminal then we can run the following command:
```
rtabmap-databaseViewer ~/.ros/rtabmap.db
```  
![][image1]

### Results:
* Kitchen And Dining Scene:    
![][image3]
![][image4]
![][image2]  

* Willowgarage Scene:

RTAB-Map                   | RTAB-Map
:-------------------------:|:-------------------------:
![][image6]                | ![][image10] 
  
![][image8]
![][image9]

Willowgarage Top           | Hsin Bot In Willowgarage
:-------------------------:|:-------------------------:
![][image11]                | ![][image12] 
  
![][image5] 

### Future Work - Applies RTAB Mapping To A Real Robot:

Intel aero flying car      | RTAB-Map
:-------------------------:|:-------------------------:
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/qXfB4bgf53A/0.jpg)](https://youtu.be/qXfB4bgf53A) |  [![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/rF9DJFgUhv0/0.jpg)](https://youtu.be/rF9DJFgUhv0) 

