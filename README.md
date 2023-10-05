# project_simulation

__Installation__

___Required packages:___

[Universal Robots](https://github.com/ros-industrial/universal_robot/tree/melodic-devel)

[Table Base](https://drive.google.com/drive/folders/100JuX8GpcT_u2RUbGYeqLP7rtylO5HOu?usp=sharing)


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