
# mobile_aloha_sim

![aloha](./doc/aloha.png)



## test environment

Ubuntu 20.04

ros noetic

gazebo version 11

## Compile

``` bash
mkdir aloha_sim_ws
cd aloha_sim_ws
mkdir src
cd src
git clone https://github.com/agilexrobotics/mobile_aloha_sim
cd ..
catkin_make
```

## File Directory

```
├── aloha_description
│ ├── aloha
│ ├── arx5_description
│ ├── arx5-urdf
│ │ ├── arx5
│ │ └── arx5p2
│ ├── livox_laser_simulation
│ └── tracer
│ ├── image
│ ├── tracer_description
│ └── tracer_gazebo_sim
├── aloha_mujoco
| └── aloha
| ├── CMakeLists.txt
| ├── meshes_mujoco
| │ ├── aloha_v1.xml
| │ └── meshes_mujoco
| ├── package.xml
| └── scripts
| ├── aloha_ctrl.py
| └── aloha_ctrl_test.py
├── arx5_moveit_config
│ ├── config
│ └── launch
└── doc
```

Among them, aloha_mujoco is the simulation under mujocoaccomplish,specificpleaseRefer to aloha_mujoco filefolder[README](./aloha_mujoco/README.MD)

## Start the simulation

### Gazebo Simulation

``` bash
roslaunch arx5_moveit_config demo_gazebo.launch
```

![aloha_gazebo](./doc/aloha_gazebo.png)



![aloha_rviz](./doc/aloha_rviz.png)



startGazeboAfter the simulation, there are two windows, one is the gazebo physical simulation window, and the other is the rviz window. In the rviz window, you canTuneUse MoveItGroupItemregulationRowing robot arm

In the gazebo simulation window, rightsideGraphicsShowIt showsreal timePhysical simulationringenvironment, the position information of the robot arm and its operationmoveLearning ModelSimulationThe information is allthisinsideShowGazebo will also reflectFeedSimulated robotic armstate,ExecutionOKregulationScratcherhairControl angle of delivery

In the rviz simulation window, the lower leftSide DisplayIt shows moveitGroupThe ui interface of the software,thisYou canchoosedifferentregulationDrawPlanning GroupTo control different robotic arms andfolderClaw. RightsidewindowShowIt showsreal timeThe position of the robot arm,thisThe first one is provided by gazebo simulation

#### Mobile chassis

``` bash
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```

OpenkeyboardcontrolFestivalClick, you can downloadhairSpeed control bottomplateshiftmove

#### Mobile Robotic Arm

Drag in the rviz interfacemoveTeaching ball, presspictureAs shown in the operation, the robot arm willStandardEndfolderClaw position,countCalculate the levelFestivalAngle and Robotic Armrailtrace

![aloha_move](./doc/aloha_moveit_1.png)

It should be noted that whenClick PlanstartregulationAfter the plan,SystemneedTime meterCalculate, wait for Execute buttonkeyBy GrayIntoBlack, dotshitYou canExecutionOKJusttalentcountRowrailtrace.

### rviz simulation

The only difference between rviz simulation and gazebo simulation is that the physical simulation engine gazebo is not started, but only the data visualization platform rviz is started

``` bash
roslaunch arx5_moveit_config demo.launch
```

startmoveThen the rviz interface in gazebo simulationSample, just follow the above steps.



##isaac sim simulation

### isaac sim download

https://developer.nvidia.com/isaac-sim Click to download omniverse, then search for isaac sim in the "Exchange/Exchange" of omniverse_launcher and download isaac sim

BookstorehouseProvides isaac sim simulationguideInput urdf: aloha_isaac_sim/urdf/arx5_description_isaac.urdf

Launch in omniverse_launcherIsaac sim, then the tool aboveUtils->workflows->URDF Importer->existbombIn the window that appears, find Import->Input File belowSelect urdfPath->PointClick Import

guideThe effect after entering isaac sim is as follows:

![issac_sim](./doc/aloha_isaac.png)
