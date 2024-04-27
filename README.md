# project_simulation

__Installation__

___Required packages:___

[Universal Robots](https://github.com/ros-industrial/universal_robot/tree/melodic-devel)

[Table Base](https://drive.google.com/file/d/1c9ZnxWPkZuW1fpoFA4F0t_5Hy8A91uP6/view?usp=sharing)

[Innok Heros](https://github.com/innokrobotics/innok_heros_description/tree/noetic)

**Note:** Please do not clone the repository, it clones the repo with some missing files. Instead, download as zip and change it's name as 'innok_heros_description'

[Gazebo Link Attacher Package](https://github.com/pal-robotics/gazebo_ros_link_attacher)

[Robot Localization EKF](https://github.com/cra-ros-pkg/robot_localization.git)

**Impotant:** It requires a package called GeographicLib, install from [here](https://geographiclib.sourceforge.io/C++/doc/install.html)

__Usage of Packages__

___Multirobot bringup launch___

```
roslaunch multirobot_gazebo mr_complete.launch

```
It opens a gazebo environment, spawns the robot arms into that environment and starts their controllers.

___Multirobot MoveIt! package___

After the bringup launch, users can activate Trajectory planner, pipelines and controllers for MoveIt! by executing the following code in an other terminal:

```
roslaunch multirobot_v1_moveit_config moveit_planning_context.launch

```

Launching the RViz environment. (Please run the following code in an other terminal)

```
roslaunch multirobot_v1_moveit_config moveit_rviz.launch

```

---

__Launching gazebo with a mobile arm and a fixed arm__

```
roslaunch multirobot_gazebo mr_1fixed_1mobile.launch

```

__MoveIt! packages for the mobile arm__

```
roslaunch mobile_arm_moveit_config moveit_planning_context.launch sim:=true

```

Execute in another terminal:

```
roslaunch mobile_arm_moveit_config moveit_rviz.launch

```

__MoveIt! packages for the fixed arm__

```
roslaunch fixed_arm_moveit_config moveit_planning_context.launch sim:=true

```

Execute in another terminal:

```
roslaunch fixed_arm_moveit_config moveit_rviz.launch

```