# ROS packages for the ABB YuMi (IRB14000) robot



For documentation, and instructions on how to install and employ this package, check [our wiki](https://github.com/kth-ros-pkg/yumi/wiki).

My packge is built under environment below:
ROS-melodic
Ubuntu 18.04
Use RWS control

It is really annoying that ABB has several different packages for robot control, eg abb/abb-robot-driver/abb-libegm...

Here is a list of packages that we added and compiled to control live yumi:

1. abb_egm_rws_managers
2. abb_libegm
3. abb_librws
4. abb_robot_driver
5. industrial_core

Remerber to build with catkin_make_isolated or catkin build. Also, build all others packages before yumi.

As mentioned in the kth-ros-pkg/yumi/wiki, the parameters MAX_NUM_JOINTS of industrial_core/simple_message/include/simple_message/joint_data.h must have a value of 20 for RWS control.

Here we applied the RWS control with:

roslaunch yumi_launch yumi_traj_pos_control.launch

roslaunch yumi_moveit_config demo_online.launch


More details about live robot control could be found here: https://github.com/kth-ros-pkg/yumi/wiki/Live-robot
