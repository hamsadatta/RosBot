## Packages description 

### rosbot_description

This package consits of the URDF(Unified Robot Description Format) files for the robot.

The robot is realized in rosbot.xacro file and the rosbot_ngpu.xacro file has the support for non-GPU(ngpu) systems.

The meshes folder has the support file hokuyo.dae for adding laser sensor model plugin

The packege has other launch files to visualize the robot in rviz which internally utilize the rosbot.xacro file

### rosbot_gazebo	

This package consits of the world and launch files for the gazebo simulation.

The rosbot_world.launch file imports files from rosbot_description packages.

The world folder consists of different world files for gazebo.

All world files should be saved in this directory.

### rosbot_navigation

This package consits of the configuraiton,maps and launch files for the robot navigation.

The config folder has the parameter files that are required for navigation.

The launch folder has the launch files for gmapping,hector,RTAB and amcl to realize autonomus navigation.

The maps folder has all the maps that are saved during mapping session using mapserver command.
