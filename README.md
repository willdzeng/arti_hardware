# arti_hardware
The Hardware ROS package for ARTI3 robot
## How to install
sudo apt-get install ros-$ROS_DISTRO-serial
cd "your_workspace"/src
git clone https://github.com/transcendrobotics/arti_hardware.git
cd ..
catkin_make
## How to use it
Once you have the robot, and installed ROS and this package, you can simply do
```
roslaunch arti_hardware arit_base.launch
```
## How to control the robot
Simply just publish veloctiy command on /cmd_vel you should be able to control the robot, for example:
```
sudo apt-get install ros-$ROS_DISTRO-teleop-twist-keyboard
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```
Use the instruction to control the robot.
## Notes
1. The code was capable with odometry but we don't want to use it anyway because for track robot slippery happens a lot.
2. The hardware doesn't have velocity control, the command sends to the robot is open loop, works as voltage command.
## Aurthor: Di Zeng