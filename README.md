# BUILD

In a shell : 

```
cd
mkdir -p ros/imredd/src
cd ros/imredd/
source /opt/ros/$ROS_DISTRO/setup.bash
catkin init
cd src
git clone https://github.com/pdaelm/imredd_mushr_map_test.git
cd imredd_mushr_map_test
#sudo apt update
#sudo apt install python3-vcstool
vcs import ../. < .rosinstall 
rosdep install -ir --from-paths .
cd ../..
catkin_make
source devel/setup.bash
```

# RUN 

In three different shells:

```
roslaunch mushr_sim teleop.launch
roslaunch mushr_rhc_ros imredd_map_integration.launch
rviz
```