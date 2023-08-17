# RPLidar Hector SLAM
Using Hector SLAM without odometry data on a ROS system with the RPLidar A1.

1. Install ROS full desktop version (tested on Kinetic) from: http://wiki.ros.org/kinetic/Installation/Ubuntu
2. Create a catkin workspace: http://wiki.ros.org/ROS/Tutorials/CreatingPackage
3. Clone this repository into your catkin workspace
4. In your catkin workspace run `source /devel/setup.bash`
5. Run `chmod 666 /dev/ttyUSB0` or the serial path to your lidar
6. Run `roslaunch rplidar_ros rplidar.launch`
7. Run `roslaunch hector_slam_launch tutorial.launch`
8. RVIZ should open up with SLAM data

# notes : 
Open 3 terminals :
1. Terminal 1 :
```bash
rosrun tf static_transform_publisher 0 0 0 0 0 0 1 map world 5
```
2. Terminal 2:
```bash
source devel/setup.bash
roslaunch rplidar_ros rplidar.launch
```
3. Terminal 3:
```bash
source devel/setup.bash
roslaunch hector_slam_launch tutorial.launch
```
note :

every command run in catkin_ws

check if lidar is connected or not
```bash
sudo chmod 666 /dev/ttyUSB0
```

