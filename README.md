# RosBot (An Autonomous Navigation Ambition Project)
This Repo contains launch files for Gmapping, Hector Map and Rtab Map. 
It also includes launch files for Gazebo simulations as well as Real-time hardware implementation.


Note, we modified our model to navigate a bit better. For example, we added an extra caster wheel to reduce bouncing laser during abrupt stops.Also added the depth camera plugin for RTAB-MAP. We understand that our robot model requires additional tweaking as it has some weird navigational kinks, but most of the problems are properly tuned in config files. Any suggestions would be appreciated. Nevertheless, our model is sufficient for playing with the ROS navigation stack. 

**STEP FOR RUNNING SIMULATION**
 
 **GMAPPING**
 
 **Creating the Map**

Run the following commands below. Use the teleop to move the robot around to create an accurate and thorough map.

In Terminal 1, launch the Gazebo world

`roslaunch mybot_gazebo mybot_world.launch`

In Terminal 2, start map building

`roslaunch mybot_navigation gmapping_demo.launch`


In Terminal 3, launch rviz and set the following parameters:

`roslaunch mybot_description mybot_rviz_gmapping.launch`


In Terminal 4, start teleop

`rosrun teleop_twist_keyboard teleop_twist_keyboard.py`


**Saving the Map**

In Terminal 5, save the map to some file path

`rosrun map_server map_saver -f ~/mybot_ws/src/mybot_navigation/maps/test_map`


**Loading the Map**

Close all previous terminals and run the following commands below. Once loaded, use rviz to set navigation waypoints and the robot should move autonomously.

In Terminal 1, launch the Gazebo world

`roslaunch mybot_gazebo mybot_world.launch`


In Terminal 2, start map building

`roslaunch mybot_navigation amcl_demo.launch`


In Terminal 3, launch rviz

`roslaunch mybot_description mybot_rviz_amcl.launch`




**HECTOR MAPPING**

**Creating the Map**

Run the following commands below. Use the teleop to move the robot around to create an accurate and thorough map.

In Terminal 1, launch the Gazebo world

`roslaunch mybot_gazebo mybot_world.launch`

In Terminal 2, start map building

`roslaunch mybot_navigation tutorial.launch`


In Terminal 3, launch rviz and set the following parameters:

`roslaunch mybot_description mybot_rviz_gmapping.launch`


In Terminal 4, start teleop

`rosrun teleop_twist_keyboard teleop_twist_keyboard.py`


**Saving the Map**

In Terminal 5, save the map to some file path

`rosrun map_server map_saver -f ~/mybot_ws/src/mybot_navigation/maps/hector_map`


**Loading the Map**

Close all previous terminals and run the following commands below. Once loaded, use rviz to set navigation waypoints and the robot should move autonomously.

In Terminal 1, launch the Gazebo world

`roslaunch mybot_gazebo mybot_world.launch`


In Terminal 2, start map building

`roslaunch mybot_navigation amcl_demo.launch`


In Terminal 3, launch rviz

`roslaunch mybot_description mybot_rviz_amcl.launch`




**RTAB MAPPING**

**Creating the Map**

Run the following commands below. Use the teleop to move the robot around to create an accurate and thorough map.

In Terminal 1, launch the Gazebo world

`roslaunch mybot_gazebo mybot_world.launch`

In Terminal 2, start map building

`roslaunch mybot_navigation rtab.launch`


In Terminal 3, launch rviz and set the following parameters:

`roslaunch mybot_description mybot_rviz_gmapping.launch`


In Terminal 4, start teleop

`rosrun teleop_twist_keyboard teleop_twist_keyboard.py`


**Saving the Map**

Map server is not required in RTAB-MAP 


**Loading the Map**

Close all previous terminals and run the following commands below. Once loaded, use rviz to set navigation waypoints and the robot should move autonomously.

In Terminal 1, launch the Gazebo world

`roslaunch mybot_gazebo mybot_world.launch`


In Terminal 2, start map building

`roslaunch mybot_navigation rtab.launch localization:=true`


In Terminal 3, launch rviz

`roslaunch mybot_description mybot_rviz_amcl.launch`




