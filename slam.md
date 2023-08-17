terminal 1 :
rosrun tf static_transform_publisher 0 0 0 0 0 0 1 map world 5

new terminal 2:
source devel/setup.bash
roslaunch rplidar_ros rplidar.launch

new terminal 3:
source devel/setup.bash
roslaunch hector_slam_launch tutorial.launch

note :
every command run in catkin_ws
check if lidar is connected or not
sudo chmod 666 /dev/ttyUSB0

