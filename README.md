usv_navigation

Navigation pkg for USVs and under-actuated mobile robot in plane based on ros navigation stack  
1. Modify the global base planner interface for advanced A* which considers the orientation limitation of under-actuated mobile robot and this navigation stack is available without kinetic model.  
2. In origin navigation stack, the global path planned by global planner is only used as a reference for local planner. However, in this navigation stack, global path should be followed by robot.  
3. USV will avoid obstacle when followed path is blocked by dynamic or unknown obstacle in environment. After the space is free for USV, a new global path will be planned.

Origin navigation stack: https://github.com/ros-planning/navigation

Address of simulation package: https://github.com/wangzhao9562/my_nav_test

Simulation with turtlebot: 
Find responding ros package from https://github.com/turtlebot and compile it in catkin space  
or sudo apt-get install ros-ros_version-turtlebot*

Notice: 
1. For using existed simulation tools and third-part libraries, package name is not modifed to satiesfy with the demand of interface(name is still move_base), please don't mix this package with origin navigation stack in one catkin space.
2. Programe is developed based on origin navigation stack in version of kinetic devel, the recommended system version is ubuntu 16.04LTS.

Frame of new navigation stack:  
![](https://github.com/wangzhao9562/usv_navigation/blob/master/assets/Frame_of_navigation_stack.png)  
  
  
Inner infrastructure of local planner:  
![](https://github.com/wangzhao9562/usv_navigation/blob/master/assets/Inner_infrastructure_of_local_planner.png)  
  
  
State transform of move_base node:  
![](https://github.com/wangzhao9562/usv_navigation/blob/master/assets/State_transform_of_move_base.png)  

Screenshot of simulation:  
![](https://github.com/wangzhao9562/usv_navigation/blob/master/assets/screenshot_for_nav_pub.png)  
![](https://github.com/wangzhao9562/usv_navigation/blob/master/assets/screenshot_for_nav_pub_02.png)  
![](https://github.com/wangzhao9562/usv_navigation/blob/master/assets/screenshot_for_nav_pub_03.png)  
![](https://github.com/wangzhao9562/usv_navigation/blob/master/assets/screenshot_for_nav_pub_04.png)