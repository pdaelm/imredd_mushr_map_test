# INSTALL

In a shell : 

'''
cd

mkdir -p ros/imredd/src

cd ros/imredd/

source /opt/ros/$ROS_DISTRO/setup.bash

catkin init

cd src

git clone https://github.com/pdaelm/imredd_mushr_map_test.git

cd imredd_mushr_map_test

sudo apt updatesudo apt install python3-vcstool

vcs import . < .rosinstall 

rosdep install -i --from-paths .

cd ../..

catkin build

'''

# RUN 

In three different shells:
- roslaunch mushr_sim teleop.launch
- roslaunch mushr_rhc_ros sim.launch
- rviz

# SETTINGS

