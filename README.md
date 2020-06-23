# Test: Obstacle detection and avoidance
## Installation:
```
cd my_catkin_ws
wget https://raw.githubusercontent.com/ipa-rwu/araig_simulation/araig_simulation.rosinstall.melodic
rosinstall src/. .araig_simulation.rosinstall.melodic

rosdep install --from-path src/ -i -y -r

catkin_make (or catkin build)

source devel/setup.bash
```
## steps: 
```
export ROBOT=raw3-3
export ROBOT_ENV=mobile-robot-obstacle
roslaunch araig_bringup_sim robot.launch
```
### for static obstacle:
```
roslaunch araig_objects spawn_object_urdf.launch object:=static_obstacle
```

### for moving obstacle:
```
rostopic pub /world/floor_to_belt_joint_velocity_controller/command std_msgs/Float64 "data: 10.0"
("data" here means speed)
```
