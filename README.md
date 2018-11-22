# ProAut Radar

## Introduction

This package was designed to read can messgae from Usb-PEAK, and seperate the measurement results for each target and publish the data on 'radar_messages' topic, also another topics for each message A,B 'can_messages_A' , 'can_messages_B' respectively. not only this, but also but also publish the result to point cloud standard message on 'radar_Pcd' .

The package can handle :
* [can_msgs/Frame ](http://docs.ros.org/api/can_msgs/html/msg/Frame.html)


## Node

```
rosrun radar_pa radar_pa_node
rosrun radar_pa radar2pcd_Node

```

### Input and Output Topics:

Topic Name            | Type                                                                                                   | Description
----------------------|--------------------------------------------------------------------------------------------------------|---------------------------------
"received_messages"   | [can_msgs/Frame ](http://docs.ros.org/api/can_msgs/html/msg/Frame.html)                                | Input as can_msgs / Frame .Will be converted to radar_msg type.
"radar_messages"      | radar_pa_msgs/radar_msg                                                                                | Input as radar_msg type . Will be converted to new pointcloud type.
"radar_messages"      | radar_pa_msgs/radar_msg                                                                                | Output as radar_msg type .
"radar_Pcd"           | [sensor_msgs/PointCloud ](http://docs.ros.org/melodic/api/sensor_msgs/html/msg/PointCloud.html)        | Output as PointCloud.


## Links and packages

Source code at github:
> https://github.com/TUC-ProAut/ros_radar

Related packages:
> https://github.com/ros-industrial/ros_canopen

ROS packages: (upcoming)
> ros-indigo-radar-pa
> ros-kinetic-radar-pa
> ros-lunar-radar-pa


## ROS Build-Status and Documentation

ROS-Distribution | Build-Status                                                                                                                                                    | Documentation
-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------
Indigo           | [![Build Status](http://build.ros.org/buildStatus/icon?job=Idev__radar_pa__ubuntu_trusty_amd64)](http://build.ros.org/job/Idev__radar_pa__ubuntu_trusty_amd64/) | [docs.ros.org](http://docs.ros.org/indigo/api/radar_pa/html/index.html)
Jade             | EOL May 2017                                                                                                                                                    | [docs.ros.org](http://docs.ros.org/jade/api/radar_pa/html/index.html)
Kinetic          | [![Build Status](http://build.ros.org/buildStatus/icon?job=Kdev__radar_pa__ubuntu_xenial_amd64)](http://build.ros.org/job/Kdev__radar_pa__ubuntu_xenial_amd64/) | [docs.ros.org](http://docs.ros.org/kinetic/api/radar_pa/html/index.html)
Lunar            | [![Build Status](http://build.ros.org/buildStatus/icon?job=Ldev__radar_pa__ubuntu_xenial_amd64)](http://build.ros.org/job/Ldev__radar_pa__ubuntu_xenial_amd64/) | [docs.ros.org](http://docs.ros.org/lunar/api/radar_pa/html/index.html)
